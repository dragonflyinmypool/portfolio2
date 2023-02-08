<script>
	import Columns from './Columns.svelte';
	import { projects } from './data/projects.json';
	console.log(projects);

	// create three arrays based on the status of the project
	const futureTasks = projects.filter((project) => project.status === 'todo');
	const workingOn = projects.filter((project) => project.status === 'workingOn');
	const done = projects.filter((project) => project.status === 'done');
</script>

<section class="grid">
	<Columns title="Future Tasks" arrayOfProjects={futureTasks} />
	<Columns title="Working On" arrayOfProjects={workingOn} />
	<Columns title="Done" arrayOfProjects={done} />
</section>

<style>
	.grid {
		max-width: 1200px;
		margin-top: 20px;
		display: grid;
		grid-template-columns: repeat(3, minmax(275px, 500px));
		grid-gap: 25px;
	}

	@media screen and (max-width: 900px) {
		.grid {
			grid-template-columns: 1fr;
		}
	}
</style>
