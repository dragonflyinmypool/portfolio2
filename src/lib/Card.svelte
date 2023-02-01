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
	<span>{data.links}</span>
</div>

<style>
	.card {
		padding: 1rem;
	}
</style>
