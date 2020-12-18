<style>
	.header{
		width: 100%;
		display: grid;
		grid-template-columns: 30% 30% 30%;
	}
</style>
<script>
	import Section from './section.svelte';
</script>
<div class="header">
	<Section class="section" name="Info" />
	<Section class="section" name="Games"/>
	<Section class="section" name="About"/>
</div>