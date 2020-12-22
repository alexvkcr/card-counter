<script>
	import Headerz from "./headerz.svelte";
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

<Headerz />
<body />
