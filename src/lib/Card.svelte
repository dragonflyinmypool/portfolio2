<script>
	export let data;
	import GenericCard from './GenericCard.svelte';
	import StatusBar from './infoCards/StatusBar.svelte';
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
		<div class="flex-Text">
			{#each data.links as link}
				<a href={link[1]} class="link">{link[0]}</a>
			{/each}
		</div>
	</div>
</GenericCard>

<style>
	.layout {
		display: grid;
		grid-template-rows: 40px 30px 100px 25px 30px;
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

	.link {
		border-radius: 0.4rem;
		background-color: var(--button-color);
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
