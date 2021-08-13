<script>
	import Dashboard from "./Componentes/Dashboard.svelte";
	import Header from "./Componentes/Header.svelte";

	let notes = [
		{
			id:0,
			title:'Vacaciones',
			color: 'yellow',
			text:'Hola'
		}
	];
	let copyNotes = [];
	let count = notes.length;
</script>

<main>
	<Header />
		<div>{count} Nota</div>
	<Dashboard />
</main>

