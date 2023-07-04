<script>
	import children from './data.json';
	import Folder from './Folder.svelte';

	// https://sveltematerialui.com/demo/tabs/
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<Folder name="Home" subcategories={children} />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		flex: 0.6;
	}
</style>
