<script lang="ts">
	import { base } from '$app/paths';
</script>

<div class="front-banner">
	<h1 class="banner" style="top:-2vw">RUN FOR THE HILLS</h1>
	<h1 class="banner" style="animation-delay: 6000ms;left:-52vw;top:-2vw">RUN FOR THE HILLS</h1>
</div>

<section class="featured-show" aria-label="Featured show">
	<img
		class="show-poster"
		src="{base}/images/release_2026.jpg"
		alt="Girly & the Pops release show at The Jungle on Friday, August 28th"
	/>
</section>

<style>
	.featured-show {
		position: relative;
		z-index: 1;
		display: flex;
		justify-content: center;
		margin-top: 10vh;
		padding: 0 1rem 3rem;
	}

	.show-poster {
		display: block;
		width: min(90vw, 600px);
		height: 100%;
	}
</style>
