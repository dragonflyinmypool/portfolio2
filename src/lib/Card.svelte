<script>
	export let data;
	import GenericCard from './GenericCard.svelte';
	import StatusBar from './StatusBar.svelte';
	import LinkBar from './LinkBar.svelte';
</script>

<GenericCard>
	<div class="layout">
		<h3>
			{data.title}
		</h3>
		<StatusBar statusData={data.status} />
		<p>{data.description}</p>
		<div class="flex-Text small-text">
			{#each data.techologies as tech}
				<div class="tech">{tech}</div>
			{/each}
		</div>
		<LinkBar {data} status="small" />
	</div>
</GenericCard>

<style>
	.layout {
		display: grid;
		grid-template-rows: 40px 30px 90px 30px 15px;
		font-size: 0.9rem;
	}
	h3 {
		font-size: 1.5rem;
		font-weight: 1000;
		font-family: myFirstFont;
	}

	.flex-Text {
		display: flex;
		flex-direction: row;
		justify-content: flex-start;
		gap: 0.8rem;
		padding-top: 0.5rem;
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
