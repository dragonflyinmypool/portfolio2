<script>
	export let data;
</script>

<div class="card">
	<h3>
		{data.title}
	</h3>
	<div class="status">{data.status}</div>
	<p>{data.description}</p>
	<div class="flex-Text small-text">
		{#each data.techologies as tech}
			<div class="tech">{tech}</div>
		{/each}
	</div>
	<div class="flex-Text">
		{#each data.links as link}
			<a href={link[1]} class="link">{link[0]}</a>
		{/each}
	</div>
</div>

<style>
	.card {
		padding: 0.25rem 0.75rem;
		/* border: #00b179 2px solid; */
		border-radius: 10px;
		height: 250px;
		display: grid;
		grid-template-rows: 40px 30px 105px 25px 35px;
		background-color: rgb(226, 226, 226);
	}
	h3 {
		font-size: 1.5rem;
		font-weight: 1000;
		font-family: myFirstFont;
	}
	.status {
		line-height: 30px;
	}
	.flex-Text {
		display: flex;
		flex-direction: row;
		justify-content: flex-start;
		gap: 0.8rem;
		padding-top: 0.5rem;
	}

	.link {
		border-radius: 0.4rem;
		background-color: #457c8d;
		line-height: 22px;
		height: 22px;
		padding: 0 0.3rem;
		font-size: small;
		vertical-align: middle;
	}

	.tech {
		line-height: 1rem;
	}

	a {
		color: white;
		text-decoration: none;
	}

	.small-text {
		font-size: 0.7rem;
	}
</style>
