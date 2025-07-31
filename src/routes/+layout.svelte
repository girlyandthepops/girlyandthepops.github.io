<script lang="ts">
	import { base } from '$app/paths';
	import '$lib/../app.css';
	import CustomNavbar from '$lib/components/CustomNavbar.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>
<div style="min-height: 100vh; display: flex; flex-direction: column;">
	<CustomNavbar />
	<div style="display:flex;flex-direction:column">
		{@render children()}
	</div>
	<Footer />
</div>
