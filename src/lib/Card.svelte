<script>
	export let data;
</script>

<div class="card">
	<h3>
		{data.title}
	</h3>
	<span>{data.status}</span>
	<p>{data.description}</p>
	<span>{data.techologies}</span>
	<span class="links">
		{#each data.links as link}
			<a href={link[1]}>{link[0]}</a>
		{/each}
	</span>
</div>

<style>
	.card {
		padding: 1rem;
	}
	.links {
		display: flex;
		flex-direction: row;
		justify-content: flex-start;
		gap: 1rem;
	}
</style>
