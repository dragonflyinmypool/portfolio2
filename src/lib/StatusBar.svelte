<script>
	export let statusData;
</script>

<div class="status">
	{#each statusData as status}
		<span class={status}>{status}</span>
	{/each}
</div>

<style>
	.status {
		line-height: 30px;
	}
	.Dev {
		border: 1px solid var(--green-badge);
		padding: 2px 7px;
		border-radius: 5px;
		color: var(--green-badge);
		margin-left: 10px;
	}
	.Issues {
		border: 1px solid var(--red-badge);
		padding: 2px 7px;
		border-radius: 5px;
		color: var(--red-badge);
		margin-left: 10px;
	}
</style>
