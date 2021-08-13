<script>
	import NotePlaceholder from './NotePlaceholder.svelte';
	import Nota from './Nota.svelte';
    export let note;

</script>

<div class="Dashboard">

    <div class="Notes-container">
        <NotePlaceholder on:click/>
        {#each note as note}
            <Nota title={note.title} color={note.color} text={note.text}/>
        {/each}
    </div>

    
</div>

<style>
    .Dashboard{
        width: 100%;
        padding: 20px;
        box-sizing: border-box;
    }

    .Notes-container{
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        width: 100%;
        gap: 10px;
    }
</style>