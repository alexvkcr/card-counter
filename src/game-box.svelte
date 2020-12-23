<style>
	:global(body.dark-mode) .box {
		color: white;
		border: 1px solid whitesmoke;
	}
	.box {
		width: 280px;
		min-height: 500px;
		border: 1px solid #aaa;
		border-radius: 2px;
		box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.1);
		margin: 0 auto;
	}

	/*Mobile first*/
	@media only screen and (min-width: 410px) {
		.box {
			width: 80%;
		}
	}
	@media only screen and (min-width: 600px) {
		.box {
			width: 480px;
		}
	}
</style>

<div class="box">
	<slot />
</div>
