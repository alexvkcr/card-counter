<script>
	import Headerz from "./headerz.svelte";
	import Card from "./card.svelte";
	let activeSection = "info";
</script>

<style>
	* {
		font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto,
			Oxygen, Ubuntu, Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
	}

	:global(body.dark-mode) {
		background-color: black;
		color: white;
	}
</style>

<Headerz bind:activeSection />
<body>
	<main>
		<Card type={activeSection} />
	</main>
</body>
