<script>
	import Card from './Card.svelte';

	export let title;
	let color;
	if (title === 'Future Tasks') {
		color = 'rgb(81, 73, 111)';
	} else if (title === 'Working On') {
		color = 'rgb(62, 110, 110)';
	} else if (title === 'Done') {
		color = 'rgb(33, 106, 14)';
	}

	export let arrayOfProjects;
</script>

<section class="toDo">
	<h2 style="background-color:{color}">{title}</h2>
	<div class="cardColumn">
		{#each arrayOfProjects as project}
			<Card {project} {color} />
		{/each}
	</div>
</section>

<style>
	h2 {
		text-align: center;
		border-radius: 5px;
	}

	.cardColumn {
		background-color: #212121;
		border-radius: 5px;
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		gap: 10px;
		margin-top: 10px;
	}
</style>
