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
</GenericCard>

<style>
	ul {
		padding: 15px;
	}
</style>
