<div class="card desc">
	<slot />
</div>

<style>
	.card {
		padding: 25px;
		border-radius: 30px;
		background-color: var(--nearBlack);
		height: 465px;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
	}

	.desc {
		border: 2px solid rgb(255, 255, 255);
	}

	.prod {
		border: 3px solid var(--purple);
	}
</style>
