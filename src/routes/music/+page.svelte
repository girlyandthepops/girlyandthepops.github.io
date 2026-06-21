<script lang="ts">
	import Music from '$lib/components/Music.svelte';
	import { base } from '$app/paths';
</script>

<div
	class="bg-grey rounded-2xl border-2 shadow-2xl"
	style="margin-bottom:2em;padding:1.5em;margin:auto;width:min(800px,80vw);height:1000px;display:flex;flex-direction:column"
>
	<iframe
		title="ctrl"
		data-testid="embed-iframe"
		style="border-radius:12px"
		src="https://open.spotify.com/embed/track/4mT08gSTaLkTXGurepipl0?utm_source=generator&si=5d34037e381449a5"
		width="100%"
		height="100%"
		frameBorder="0"
		allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
		loading="lazy"
	></iframe>
	<div style="height:10em"></div>
	<iframe
		title="Live at 246"
		data-testid="embed-iframe"
		style="border-radius:12px"
		src="https://open.spotify.com/embed/album/4lql69eMl6gZxtnutKHtsR?utm_source=generator"
		width="100%"
		height="200%"
		frameBorder="0"
		allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
		loading="lazy"
	></iframe>
	<div style="height:10em"></div>
	<iframe
		title="Missed Calls from Girly"
		data-testid="embed-iframe"
		style="border-radius:12px"
		src="https://open.spotify.com/embed/album/4MnUfn0eBVUkdhpGRrdrfv?utm_source=generator"
		width="100%"
		height="200%"
		frameBorder="0"
		allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture"
		loading="lazy"
	></iframe>
</div>
