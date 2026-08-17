<script lang="ts">
	import { base } from '$app/paths';
	import { DarkMode, Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
	import Music from '$lib/components/Music.svelte';
</script>

<div class="sticky top-0 z-50">
	<Navbar
		class="bg-grey"
		style="border-color:transparent; border-bottom-width:3px;background-color: rgba(0, 0, 0, 0.7);height:min(7.5em, 30vw);z-index:20"
	>
		<NavBrand href="{base}/">
			<span class="dark:text-white; self-center text-xl font-semibold whitespace-nowrap"
				><h1
					style="font-size: min(1.5em, 6vw);color:white;text-align:center;transform:translateY(-20%)"
				>
					girly & the pops
				</h1>
				<div class="flex space-x-5">
					<Music />
				</div>
			</span>
		</NavBrand>
		<NavHamburger style="color:white" />
		<NavUl ulClass="bg-black md:bg-transparent dark:bg-black dark:md:bg-transparent">
			<NavLi style="font-size: min(2em, 4vw);color:white;font-weight: bold;" href="{base}/epk"
				>epk</NavLi
			>
			<NavLi style="font-size: min(2em, 4vw);color:white;font-weight: bold;" href="{base}/shows"
				>tour</NavLi
			>
			<NavLi style="font-size: min(2em, 4vw);color:white;font-weight: bold;" href="{base}/music"
				>music</NavLi
			>
			<NavLi
				style="font-size: min(2em, 4vw);color:white;font-weight: bold;"
				href="https://girlyandthepops.myshopify.com/">shop</NavLi>
			<NavLi
				style="font-size: min(2em, 4vw);color:white;font-weight: bold;rly
			"
				href="{base}/booking">booking</NavLi
			>
			<DarkMode
				ariaLabel="Toggle dark mode"
				class="background-invert text-white hover:bg-white/10 dark:text-white dark:hover:bg-white/10"
			/>
		</NavUl>
	</Navbar>
</div>
