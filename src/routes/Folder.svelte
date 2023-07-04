<script>
	import File from './File.svelte';

	export let expanded = false;
	export let name;
	export let subcategories;

	import Card from '@smui/card';
</script>

<svelte:head>
	<link rel="stylesheet" href="node_modules/svelte-material-ui/bare.css" />
</svelte:head>

<ul>
	{#each subcategories as category}
		<li>
			{#if category.subcategories}
				<div class="card-display">
					<Card padded>{category.name}</Card>
				</div>
				<svelte:self {...category} />
			{:else}
				<File {...category} />
			{/if}
		</li>
	{/each}
</ul>

<style>
	ul {
		padding: 0.2em 0 0 0.5em;
		margin: 0 0 0 0.5em;
		list-style: none;
		border-left: 1px solid #eee;
	}

	li {
		padding: 0.2em 5em;
	}
	@import 'https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css';
</style>
