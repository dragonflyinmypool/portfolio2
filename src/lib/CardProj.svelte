<div class="card proj">
	<div class="top">
		<h2>
			<slot name="header" />
		</h2>
		<div class="tags">
			<div class="status">
				<slot name="status" />
			</div>
		</div>
		<p><slot name="description" /></p>
		<slot name="list" />
	</div>

	<div class="tags">
		<div class="buttons">
			<slot name="links" />
		</div>
	</div>
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
	.proj {
		border: 3px solid var(--purple);
	}

	h2 {
		color: var(--purple);
		font-family: myFirstFont;
		font-size: 1.7em;
	}

	a {
		color: var(--white);
		text-decoration: none;
	}

	ul {
		list-style: none;
		margin: 15px 0px;
	}

	li {
		padding: 3.5px 0px;
	}
</style>
