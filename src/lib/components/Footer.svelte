<script lang="ts">
	import Music from '$lib/components/Music.svelte';
</script>

<footer
	class="bg-pink py-8 text-black"
	style="position:relative;height:200px; width: 100%;border-color:black; border-top-width:3px"
>
	<div class="container mx-auto px-4">
		<div class="flex flex-col items-center space-y-4">
			<!-- Band Name -->
			<div class="text-center text-2xl font-bold">
				girly and the pops. Art and typography by <a
					class="merC"
					style="text-decoration:underline"
					href="https://www.instagram.com/i_do_poke/?hl=en">MerC</a
				>
			</div>
			<div class="flex space-x-6">
				<Music />
			</div>
			<!-- Copyright -->
			<div class="w-full border-t border-gray-700 pt-4 text-center text-sm text-gray-400">
				<p>&copy; 2025 girly and the pops. All rights reserved.</p>
			</div>
		</div>
	</div>
</footer>

<style>
	footer {
		margin-top: auto;
	}
</style>
