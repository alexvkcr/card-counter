<script>
	import { fade } from "svelte/transition";
	import GamePlusMinus from "./games/game-plus-minus.svelte";
	import GameBox from "./game-box.svelte";

	let showing = "menu";

	function transitionPlusMinusGame() {
		showing = "gamePlusMinus";
	}
	function closeGame() {
		showing = "menu";
	}
</script>

<style>
	:global(body.dark-mode) * {
		color: white;
	}
	.games-menu {
		height: 100%;
		min-height: 100%;
		display: -webkit-box;
		display: flex;
		-webkit-box-orient: vertical;
		-webkit-box-direction: normal;
		flex-direction: column;
		align-items: stretch;
	}
	.games-menu > div {
		-webkit-box-flex: 1;
		flex: 1;

		display: flex;
		flex-direction: column;
		justify-content: center;
		border: 1px solid #ccc;
		border-radius: 2px;

		min-height: 167px;
		text-align: center;
	}
</style>

{#if showing == 'menu'}
	<GameBox>
		<div class="games-menu">
			<div on:click={transitionPlusMinusGame}>Plus minus</div>
			<div>other 1</div>
			<div>other 2</div>
		</div>
	</GameBox>
{:else if showing == 'gamePlusMinus'}
	<div transition:fade>
		<GamePlusMinus on:closeGame={closeGame} />
	</div>
{/if}
