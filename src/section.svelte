<script>
	export let name = "Default";
</script>

<style>
	.section-text {
		padding: 0 8px;
	}
	/*Mobile first*/
	@media only screen and (min-width: 600px) {
		.section-text {
			text-align: center;
		}
	}
</style>

<div class="section-text" on:click>{name}</div>
