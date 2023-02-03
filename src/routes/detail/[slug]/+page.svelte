<script context="module">
	export async function load({ fetch, params }) {
		const id = params.slug;
		const data = await fetch(`data/${params.slug}.json`).then((r) => r.json());
		console.log(data);
		return {
			props: {
				data
			}
		};
	}
</script>

<script>
</script>
