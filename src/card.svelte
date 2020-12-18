<script>
		let heart = 'heart'
		let diamond = 'diamond'
		let spade = 'spade'
		let club = 'club'
		
		export let type = spade;
</script>
<style>
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
<div class="{type}">

</div>