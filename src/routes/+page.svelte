<script>
	import Card from '$lib/Card.svelte';
	import IntroCard from '$lib/infoCards/IntroCard.svelte';
	import CourseCard from '$lib/infoCards/CourseCard.svelte';

	import pd from '$lib/data/cardData.json';
	const projectData = pd.ProductionCards;
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
