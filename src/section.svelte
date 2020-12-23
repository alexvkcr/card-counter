<script>
	export let name = "Default";
</script>

<style>
	/*Mobile first*/
	@media only screen and (min-width: 600px) {
		.section-text {
			text-align: center;
		}
	}

	.section-text {
		padding: 0 8px;
	}
</style>

<div class="section-text" on:click>{name}</div>
