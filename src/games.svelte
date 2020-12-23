<script>
	import GamePlusMinus from "./games/game-plus-minus.svelte";
</script>

<style>
	:global(body.dark-mode) * {
		color: white;
	}
	.games-menu {
		display: grid;
		grid-template-columns: 1fr;
		grid-template-rows: 1fr 1fr 1fr;
		gap: 0px 0px;
		grid-template-areas:
			"."
			"."
			".";
	}
</style>

<GamePlusMinus />
<div class="games-menu" />
<!--Aquí irá un grid con los 3 juegos-->
