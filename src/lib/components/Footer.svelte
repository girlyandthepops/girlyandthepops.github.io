<script lang="ts">
	import Music from '$lib/components/Music.svelte';
</script>

<footer
	class="py-8 text-white footer"
	style="background-color: rgba(0, 0, 0, 0.7);position:relative; bottom:0;backdrop-filter: blur(2px);"
>
	<div class="container mx-auto px-4">
		<div class="flex flex-col items-center space-y-4"
		>
			<!-- Band Name -->
			<div class="text-center text-2xl font-bold">
				girly & the pops
			</div>
			<div class="flex space-x-6">
				<Music />
			</div>
			<!-- Copyright -->
			<div class="w-full border-t border-gray-700 pt-4 text-center text-sm text-gray-400">
				<p>&copy; 2026 girly & the pops. All rights reserved.</p>
			</div>
		</div>
	</div>
</footer>

<style>
	footer {
		margin-top: auto;
	}
</style>
