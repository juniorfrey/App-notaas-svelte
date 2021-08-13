<script>
	import Header from './Header.svelte';
    export let text, color, title;
</script>
<div class="Note">

    <div class="Note-container" style={'background-color: ' + color}>
        <div class="header">
            <div class="options">
                <button>Color</button>
                <button>Eliminar</button>
            </div>
        </div>
        <div class="content">
            <div class="title">
                <input type="text" class="title" placeholder="Sin titulo" bind:value={title}>
            </div>
            <div class="text">
                <textarea bind:value={text} class="text" name="" id="" cols="30" rows="10" placeholder="Escribir ..." />
                
            </div>
        </div>

    </div>
</div>

<style>
 .Note{
     background-color: white;
     border-radius: 3px;
     border:solid 2px transparent;
     overflow: hidden;
     height: 400px;
 }

 .Note-container{
     height: 100%;
 }

 .Note:focus-within{
     border:solid 2px #000;
     box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
 }

 .Note .Note-container .header{
     padding: 5px;
 }

 .header .options{
    display: flex;
    justify-content: space-between;
 }

 .Note .content{
     padding: 0 20px;
 }

 .text textarea{
    width: 100%;
    border: 0;
    outline: none;
    resize: none;
    height: 250px;
 }

 .title input{
     font-size: 22px;
     font-weight: bold;
     padding: 10px 0;
     outline: none;
     border: none;
     width: 100%;
 }

 button{
     margin: 0;
     border: none;
     background-color: transparent;
     cursor: pointer;
 }

 textarea, input{
     background: transparent;
 }
</style>