<script>
	import { createEventDispatcher } from "svelte";

	const dispatch = createEventDispatcher();

	function closeGame() {
		dispatch("closeGame", {});
	}
</script>

<style>
	:global(body.dark-mode) * {
		color: white;
	}
</style>

<div on:click={closeGame}>x</div>
