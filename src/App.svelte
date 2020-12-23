<script>
	import Headerz from "./headerz.svelte";
	import Card from "./card.svelte";
	let activeSection = "Info";
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
	Headerz {
		max-width: 100%;
	}
</style>

<Headerz bind:activeSection />
<body>
	<main>
		<Card type={activeSection} />
	</main>
</body>
