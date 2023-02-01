<script>
	import people from '$lib/data/cardData.json';
	const projectData = people.ProductionCards;

	import Card from '$lib/Card.svelte';
	import IntroCard from '$lib/IntroCard.svelte';
	import CourseCard from '$lib/CourseCard.svelte';
</script>

<main>
	<IntroCard />
	{#each projectData as data}
		<Card {data} />
	{/each}
	<CourseCard />
</main>

<style>
	main {
		max-width: 1200px;
		margin: auto;
		width: initial;
		display: grid;
		gap: 1rem;
		grid-template-columns: repeat(auto-fit, minmax(325px, 1fr));
	}
</style>
