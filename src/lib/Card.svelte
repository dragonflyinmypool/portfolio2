<script>
	export let project;
	export let color;
</script>

<div class="card" style="background-color: {color};">
	<h3>{project.title}</h3>
	<!-- <p class="description">A web app that takes a tweet and turns it into a poem</p> -->
	<div class="buttons">
		<!-- add links based on object-->
		{#each Object.entries(project.links) as link}
			<a href={link[1]}><button style="background-color: {color};"> {link[0]} </button></a>
		{/each}
	</div>
</div>

<style>
	.card {
		height: 90px;
		display: grid;
		grid-template-rows: 40px 30px;
		padding: 10px;
		border-radius: 5px;
	}

	button {
		background-color: #212121;
		border: 1px solid #dedede;
		border-radius: 5px;
		color: #dedede;
		padding: 5px;
		cursor: pointer;
	}

	.buttons {
		display: flex;
		justify-content: flex-start;
		gap: 10px;
	}
</style>
