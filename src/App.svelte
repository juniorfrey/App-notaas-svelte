<script>
	import Dashboard from "./Componentes/Dashboard.svelte";
	import Header from "./Componentes/Header.svelte";
	import {v4} from 'uuid';

	let notes = [
		{
			id:0,
			title:'Vacaciones',
			color: 'yellow',
			text:'Hola'
		},
		{
			id:1,
			title:'Trabajo de seguridad',
			color: 'red',
			text:'Hacer trabajo de seguridad'
		}
	];
	let copyNotes = [];
	let count = notes.length;

	function handleNew(){
		const color = generateCoor();
		const id = v4();
		const note = {
			id:id,
			title:'',
			color:color,
			text:''
		};
		notes = [note, ...notes];
		copyNotes = [...notes];
	}

	function generateCoor(){
		const colors = ['#DDFFC2','#FFC2C2','#FFEAC2','#C2FFD3', '#D35400', '#1ABC9C', '#2980B9', '#8E44AD','#E74C3C', '#566573','#A3E4D7'];
		const index = Math.floor(Math.random() * (colors.length));
		return colors[index];
	}
</script>

<main>
	<Header />
		<div>{count} Nota</div>
	<Dashboard note={notes} on:click={handleNew}/>
</main>

