<script>
	// import genericCard.svelte
	import GenericCard from '../GenericCard.svelte';
</script>

<GenericCard>
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
	<div class="flex-Text">
		<a href={`./courses`} class="link">+</a>
	</div>
</GenericCard>

<style>
	ul {
		padding: 15px;
	}
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
		font-family: myFirstFont;
		text-decoration: none;
		font-weight: bold;
		border-radius: 10px;
		line-height: 12px;
	}
	a:hover {
		color: purple;
	}
</style>
