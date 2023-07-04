<script>
	import Card from '@smui/card';
	export let name;
	export let description;
	$: type = name.slice(name.lastIndexOf('.') + 1);
</script>

<svelte:head>
	<link rel="stylesheet" href="node_modules/svelte-material-ui/bare.css" />
</svelte:head>

<div class="card-display">
	<Card padded>{name} : {description}.</Card>
</div>

<style>
	.box {
		width: 300px;
		border: 1px solid #aaa;
		border-radius: 2px;
		box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.1);
		padding: 1em;
		margin: 0 0 1em 0;
	}
</style>
