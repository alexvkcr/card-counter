<script>
	import Headerz from "./headerz.svelte";
	import Module from "./module.svelte";
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
		<Module type={activeSection} />
	</main>
</body>
