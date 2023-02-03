<script>
	// import genericCard.svelte
	import GenericCard from '../../lib/GenericCard.svelte';
</script>

<GenericCard>
	<h2>Courses</h2>
	<div class="grid" />
	<div class="flex-Text">
		<a href={`../`} class="link">-</a>
	</div>
</GenericCard>

<style>
	.grid {
		display: grid;
		grid-gap: 0.1rem;
		padding: 1rem;
		background-color: #e6efea;
	}
	.grid > div {
		background-color: lightblue;
		padding: 0.6rem 0.5rem;
	}
</style>
