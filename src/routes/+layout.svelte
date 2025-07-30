<script lang="ts">
    import { base } from '$app/paths';
	import '$lib/../app.css';
	import CustomNavbar from '$lib/components/CustomNavbar.svelte';
    import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();

</script>
	<CustomNavbar />
		<div style="min-height:78vh;display:flex;flex-direction:column;justify-content:center;align-items:center;">
			{@render children()}
		</div>
	<Footer />
