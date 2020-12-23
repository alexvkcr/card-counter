<style>
	/*Mobile first*/
	@media only screen and (min-width: 600px) {
		.box {
			width: 80%;
		}
	}

	:global(body.dark-mode) .box {
		color: white;
		border: 1px solid whitesmoke;
	}
	.box {
		width: 280px;
		min-height: 500px;
		max-height: 800px;

		border: 1px solid #aaa;
		border-radius: 2px;
		box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.1);
		margin: 0 auto;
	}
</style>

<div class="box">
	<slot />
</div>
