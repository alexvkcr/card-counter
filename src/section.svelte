<script>
	export let name = "Default";
</script>

<style>
	@media only screen and (min-width: 600px) {
		.section-text {
			text-align: center;
		}
	}
</style>

<div class="section-text" on:click>{name}</div>
