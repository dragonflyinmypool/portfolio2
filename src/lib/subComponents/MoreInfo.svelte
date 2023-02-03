<script>
	export let data;
</script>

<div class="flex-Text small-text">
	{#each data.techologies as tech}
		<div class="tech">{tech}</div>
	{/each}
</div>

<style>
	.flex-Text {
		display: flex;
		flex-direction: row;
		justify-content: flex-start;
		flex-wrap: wrap;
		gap: 0.5rem;
		padding-top: 0.5rem;
	}
	.tech {
		line-height: 1rem;
	}

	.small-text {
		font-size: 0.7rem;
	}
</style>
