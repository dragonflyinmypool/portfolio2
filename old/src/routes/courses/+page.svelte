<script>
	import { courses } from '$lib/data/courses.json';
</script>

<div class="page">
	<h1>Courses</h1>
	<main class="grid">
		<div class="notStarted column">
			<h2>Future Courses</h2>
			<div class="grid2">
				{#each courses as course}
					{#if course.status.toLowerCase() === 'Not Yet Started'.toLocaleLowerCase()}
						<div>
							{course.title}
							<div class="institution">{course.institution}</div>
						</div>
					{/if}
				{/each}
			</div>
		</div>
		<div class="taking column">
			<h2>Taking</h2>
			<div class="grid2">
				{#each courses as course}
					{#if course.status.toLowerCase() === 'Taking currently'.toLocaleLowerCase()}
						<div>
							{course.title}
							<div class="institution">{course.institution}</div>
						</div>
					{/if}
				{/each}
			</div>
		</div>
		<div class="completed column">
			<h2>Completed</h2>
			<div class="grid2">
				{#each courses as course}
					{#if course.status.toLowerCase() === 'Completed'.toLocaleLowerCase()}
						<div>
							{course.title}
							<div class="institution">{course.institution}</div>
						</div>
					{/if}
				{/each}
			</div>
		</div>
	</main>

	<div class="flex-Text">
		<a href={`../`} class="link">-</a>
	</div>
</div>

<style>
	h1 {
		margin-bottom: 20px;
	}
	.grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		grid-gap: 1rem;
		max-width: 1000px;
	}

	.column {
		padding: 0.5rem;
		border-radius: 10px;
	}

	.grid2 {
		display: grid;
		grid-template-columns: minmax(200px, 300px);
		grid-gap: 0.4rem;
		color: white;
		font-size: 1.2rem;
	}

	.grid2 > div {
		padding: 0.3rem 0.5rem;
		border-radius: 10px;
	}

	.completed div div {
		background-color: #358238;
	}

	/* grey border */
	.taking div div {
		background-color: rgb(133, 174, 117);
	}
	.notStarted div div {
		background-color: #888888;
	}

	.institution {
		font-size: 0.7rem;
	}
	/* Back button */
	.flex-Text {
		display: flex;
		padding-top: 0.5rem;
	}
	.link {
		background-color: #e6efea;
		padding: 0.6rem 0.5rem;
		line-height: 4px;
	}

	a {
		color: var(--title-color);
		font-family: myFirstFont;
		text-decoration: none;
		font-weight: bold;
		border-radius: 10px;
	}
</style>
