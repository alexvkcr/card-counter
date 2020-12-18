<style>
	header{
		width: 100%;
		display: grid;
		grid-template-columns: 1fr 1fr 1fr;
		grid-template-rows: 1fr 1fr ;
		grid-template-areas: 
			"a"
			"a a a";
	}
	.shapes{
		/*As a grid child*/
		grid-column: span 4;
		/*As a grid parent*/
		display: grid;
		grid-template-columns: 5px 5px 5px 5px;
		grid-column-gap: 0px;
		
		padding: 0 calc(50vw - 10px);
	}
	.heart:before {
		content: '\2665';
		color: red;
	}
	.diamond:before {
		content: '\2666';
		color: red;
	}
	.club:before {
		content: '\2663';
		color: black;
	}
	.spade:before {
		content: '\2660';
		color: black;
	}
</style>
<script>
	import Section from './section.svelte';
</script>
<header class="header">
	<div class="shapes">
		<div class="diamond"></div>
		<div class="club"></div>
		<div class="heart"></div>
		<div class="spade"></div>		
	</div>
	<Section class="section" name="Info" />
	<Section class="section" name="Games"/>
	<Section class="section" name="About"/>
</header>