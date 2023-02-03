<script>
	// import genericCard.svelte
	import GenericCard from '../../lib/GenericCard.svelte';
</script>

<GenericCard>
	<h2>Courses</h2>
	<div class="grid">
		<li>Intermediate JavaScript</li>
		<li>Understanding the Weird Parts</li>
		<li>JavaScript Algorithms and Data Structures</li>
		<li>Svelte.js, The Complete Guide by Max Schwarzmüller, Udemy</li>
		<li>
			NodeJS, The Complete Guide (MVC, REST APIs, GraphQL, Denode) by Max Schwarzmüller, Udemy
		</li>
		<li>The Complete Google Sheets Course: Beginner to Advanced!</li>
	</div>
	<div class="flex-Text">
		<a href={`../`} class="link">-</a>
	</div>

	<style>
		.flex-Text {
			display: flex;
			flex-direction: row;
			justify-content: flex-start;
			gap: 0.8rem;
			padding-top: 0.5rem;
			font-size: small;
			height: 32px;
		}
		.link {
			background-color: #e6efea;
			padding: 0.6rem 0.5rem;
			line-height: 4px;
		}

		a {
			color: var(--title-color);
			text-decoration: none;
			font-weight: bold;
			border-radius: 10px;
			line-height: 12px;
		}
		a:hover {
			color: purple;
		}
	</style>
</GenericCard>

<style>
	ul {
		padding: 15px;
	}
</style>
