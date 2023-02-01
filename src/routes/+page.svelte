<script>
	import people from '$lib/data/cardData.json';
	const projectData = people.ProductionCards;

	import Card from '$lib/Card.svelte';
	import EmptyCard from '$lib/EmptyCard.svelte';
</script>

<main>
	<EmptyCard>
		<h1>Jamie Joseph Heiney</h1>
		1990 London
		<ul style="margin-top: 20px;">
			<li>HTML, CSS, Javascript, Svelte, Node</li>
			<li>Accounting fundementals</li>
			<li>Principals of design</li>
		</ul>
	</EmptyCard>
	{#each projectData as data}
		<Card {data} />
	{/each}
	<EmptyCard>
		<h2>Courses</h2>
		<ul style="list-style:disc">
			<li>Intermediate JavaScript</li>
			<li>Understanding the Weird Parts</li>
			<li>JavaScript Algorithms and Data Structures</li>
			<li>Svelte.js, The Complete Guide by Max Schwarzmüller, Udemy</li>
			<li>
				NodeJS, The Complete Guide (MVC, REST APIs, GraphQL, Denode) by Max Schwarzmüller, Udemy
			</li>
			<li>The Complete Google Sheets Course: Beginner to Advanced!</li>
		</ul>
	</EmptyCard>
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
