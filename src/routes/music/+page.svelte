<script lang="ts">
	import Music from '$lib/components/Music.svelte';
	import { base } from '$app/paths';
</script>

<div
	class="bg-pink border-2 rounded-2xl shadow-2xl"
	style="padding:1.5em;margin:auto;width:min(600px,80vw);height:500px;display:flex;flex-direction:column"
>
	<a
		href="{base}/missed_calls_from_girly"
		class="merC"
		style="font-size:1.5em; text-decoration:underline">MISSED CALLS FROM GIRLY</a
	>
	<iframe
		data-testid="embed-iframe"
		style="border-radius:12px"
		src="https://open.spotify.com/embed/album/4MnUfn0eBVUkdhpGRrdrfv?utm_source=generator"
		width="100%"
		height="100%"
		frameBorder="0"
		allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
		loading="lazy"
	></iframe>
</div>
