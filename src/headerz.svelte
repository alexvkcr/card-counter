<script>
	import Section from "./section.svelte";
	export let activeSection;

	function switchLightMode() {
		window.document.body.classList.toggle("dark-mode");
	}

	function changeSection(element) {
		activeSection = element;
	}
</script>

<style>
	/*Mobile first*/
	@media only screen and (min-width: 600px) {
		.pos-darkmode {
		}
	}
	:global(body.dark-mode) button {
		background-color: #0084f6;
		color: rgb(242, 247, 202);
		text-shadow: 1px 1px 1px black;
	}
	header {
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
		grid-template-rows: 1fr 1fr 1fr;
		gap: 0px;
		grid-template-areas:
			". . ."
			". . ."
			". . .";
	}
	.shapes {
		/*As a grid child*/
		grid-column: span 3;
		/*As a flexbox parent*/

		display: flex;
		flex-direction: row;
		flex-wrap: nowrap;
		justify-content: center;
		align-content: center;
		align-items: center;
	}
	.pos-darkmode {
		grid-column: span 3;
		display: flex;
		width: 100%;
	}
	.dark-mode {
		margin-left: auto;
		margin-right: 2px;
		order: 2;

		-moz-box-shadow: 0px 1px 0px 0px #1c1b18;
		-webkit-box-shadow: 0px 1px 0px 0px #1c1b18;
		box-shadow: 0px 1px 0px 0px #1c1b18;
		background: -webkit-gradient(
			linear,
			left top,
			left bottom,
			color-stop(0.05, #eae0c2),
			color-stop(1, #ccc2a6)
		);
		background: -moz-linear-gradient(top, #eae0c2 5%, #ccc2a6 100%);
		background: -webkit-linear-gradient(top, #eae0c2 5%, #ccc2a6 100%);
		background: -o-linear-gradient(top, #eae0c2 5%, #ccc2a6 100%);
		background: -ms-linear-gradient(top, #eae0c2 5%, #ccc2a6 100%);
		background: linear-gradient(to bottom, #eae0c2 5%, #ccc2a6 100%);
		filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#eae0c2', endColorstr='#ccc2a6',GradientType=0);
		background-color: #eae0c2;
		-webkit-border-radius: 15px;
		-moz-border-radius: 15px;
		border-radius: 15px;
		border: 2px solid #333029;
		display: inline-block;
		cursor: pointer;
		color: #505739;
		font-family: Arial;
		font-size: 10px;
		font-weight: bold;
		padding: 6px 16px;
		text-decoration: none;
		text-shadow: 0px 1px 0px #ffffff;
	}
	.dark-mode:hover {
		background: -webkit-gradient(
			linear,
			left top,
			left bottom,
			color-stop(0.05, #ccc2a6),
			color-stop(1, #eae0c2)
		);
		background: -moz-linear-gradient(top, #ccc2a6 5%, #eae0c2 100%);
		background: -webkit-linear-gradient(top, #ccc2a6 5%, #eae0c2 100%);
		background: -o-linear-gradient(top, #ccc2a6 5%, #eae0c2 100%);
		background: -ms-linear-gradient(top, #ccc2a6 5%, #eae0c2 100%);
		background: linear-gradient(to bottom, #ccc2a6 5%, #eae0c2 100%);
		filter: progid:DXImageTransform.Microsoft.gradient(startColorstr='#ccc2a6', endColorstr='#eae0c2',GradientType=0);
		background-color: #ccc2a6;
	}
	.dark-mode:active {
		position: relative;
		top: 1px;
	}
</style>

<header class="header">
	<div class="shapes">
		<div class="diamond" />
		<div class="club" />
		<div class="heart" />
		<div class="spade" />
	</div>
	<Section name="Info" on:click={(e) => changeSection(e.target.innerText)} />
	<Section name="Games" on:click={(e) => changeSection(e.target.innerText)} />
	<Section name="About" on:click={(e) => changeSection(e.target.innerText)} />
	<div class="pos-darkmode">
		<button class="dark-mode" on:click={switchLightMode}>Dark Mode</button>
	</div>
</header>
