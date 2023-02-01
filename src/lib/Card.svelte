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
			<div class="link"><a href={link[1]}>{link[0]}</a></div>
		{/each}
	</div>
</div>

<style>
	.card {
		padding: 0.25rem 0.75rem;
		max-width: 500px;
		border: #00b179 2px solid;
		border-radius: 10px;
		height: 250px;
		display: grid;
		grid-template-rows: 40px 30px 85px 30px 40px;
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
		border-radius: 0.7rem;
		padding: 0.3rem 0.5rem;
		background-color: #00b179;
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
