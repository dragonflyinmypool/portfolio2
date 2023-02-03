<script>
	export let statusData;
</script>

<div class="status">
	{#if statusData.status}
		<span class="Dev">{statusData.status}</span>
	{/if}
	{#if statusData.version}
		<span class="Dev">V{statusData.version}</span>
	{/if}
</div>

<style>
	.status {
		line-height: 30px;
	}
	.Dev {
		border: 1px solid var(--button-color);
		padding: 2px 7px;
		border-radius: 5px;
		color: var(--button-color);
		font-weight: bold;
	}
</style>
