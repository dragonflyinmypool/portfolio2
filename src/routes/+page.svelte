<script>
	import '../app.css';
	import Card from '../lib/Card.svelte';
	import CardProj from '../lib/CardProj.svelte';
</script>

<div class="center">
	<main>
		<Card>
			<div class="top">
				<h1>Jamie Joseph Heiney</h1>
				1990 London
				<ul style="margin-top: 20px;">
					<li>HTML, CSS, Javascript, Svelte, Node</li>
					<li>Accounting fundementals</li>
					<li>Principals of design</li>
				</ul>
			</div>
		</Card>
		<CardProj>
			<span slot="header">Tweet 2 Poem</span>
			<span slot="status">Development</span>
			<span slot="description">
				Include this twitter bot's name in your tweet and it will automaticly reply with a poem
				based on your tweet.
			</span>
			<span slot="list">
				<ul class="bottom">
					<li>Node.js ~ Twitter API, GPT-3 ~ Railway.app</li>
				</ul>
			</span>
			<span slot="links">
				<a href="https://github.com/dragonflyinmypool/Tweet2Poem">Repo</a>
			</span>
		</CardProj>
	</main>
</div>
