<script>
	import About from "./about.svelte";
	import Games from "./games.svelte";
	import Info from "./info.svelte";
	export let type;
	const components = {
		Info: Info,
		Games: Games,
		About: About,
	};
</script>

<style>
	:global(body.dark-mode) * {
		color: white;
	}
</style>

<svelte:component this={components[type]} />
