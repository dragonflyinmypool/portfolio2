<script>
	import people from '$lib/cardData.json';
	const projectData = people.ProductionCards;

	import Card from '$lib/Card.svelte';
	import { loop_guard } from 'svelte/internal';
</script>

{#each projectData as data}
	<Card {data} />
{/each}
