<script>
	export let data;
	import GenericCard from './GenericCard.svelte';
	import StatusBar from './StatusBar.svelte';
	import LinkBar from './LinkBar.svelte';
	import CardTitle from './CardTitle.svelte';
</script>

<GenericCard>
	<div class="layout">
		<CardTitle {data} />

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
		grid-template-rows: 45px 120px 25px 35px;
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
