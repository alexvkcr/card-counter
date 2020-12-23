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
	.close-game {
		text-align: right;
	}
</style>

<div class="close-game" on:click={closeGame}>close game X</div>
