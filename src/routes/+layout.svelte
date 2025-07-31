<script lang="ts">
	import { base } from '$app/paths';
	import '$lib/../app.css';
	import CustomNavbar from '$lib/components/CustomNavbar.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<CustomNavbar />
<div style="min-height:calc(100vh - 270px); display:flex; flex-direction:column">
	{@render children()}
</div>
<Footer />
