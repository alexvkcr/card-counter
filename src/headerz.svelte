<script>
	import Section from "./section.svelte";

	function switchLightMode() {
		console.log(111);
		window.document.body.classList.toggle("dark-mode");
	}
</script>

<style>
	:global(body.dark-mode) button {
		background-color: #0084f6;
		color: rgb(242, 247, 202);
	}
	header {
		width: 100%;
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
		grid-template-rows: 1fr 1fr;
		grid-template-areas:
			"a"
			"a a a";
	}
	.shapes {
		/*As a grid child*/
		grid-column: span 4;
		/*As a grid parent*/
		display: grid;
		grid-template-columns: 5px 5px 5px 5px;
		grid-column-gap: 0px;

		padding: 0 calc(50vw - 30px);
	}
	.pos-darkmode {
		width: 100%;
		margin-left: calc(100% - 110px);
		margin-top: 20px;
	}
	.dark-mode {
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
	<Section class="section" name="Info" />
	<Section class="section" name="Games" />
	<Section class="section" name="About" />
</header>
<div class="pos-darkmode">
	<button class="dark-mode" on:click={switchLightMode}>Dark Mode</button>
</div>
