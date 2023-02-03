<script>
	// Components
	import ProjectCard from '$lib/ProjectCard.svelte';
	import IntroCard from '$lib/infoCards/IntroCard.svelte';
	import CourseCard from '$lib/infoCards/CourseCard.svelte';

	// Project Cards Data
	import { cards } from '$lib/data/cardData.json';
</script>

<main>
	<IntroCard />
	{#each cards as data}
		<ProjectCard {data} />
	{/each}
	<CourseCard />
</main>

<style>
	main {
		/* Set the max width, and center content */
		max-width: 1200px;
		margin: auto;

		/* Make a grid */
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(325px, 1fr));
		gap: 1rem;
	}
</style>
