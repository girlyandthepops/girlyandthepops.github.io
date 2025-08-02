<script lang="ts">
	import { base } from '$app/paths';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
</script>

<Navbar class="bg-pink" style="border-color:black; border-bottom-width:3px">
	<NavBrand href="{base}/">
		<img
			src="{base}/images/girly_in_action.png"
			style="height:3em;margin:1em;border-radius:2em"
			alt="Girly In Action"
		/>
		<span class="self-center text-xl font-semibold whitespace-nowrap dark:text-white"
			><h1 style="font-size: 1.5em">Girly & the Pops</h1></span
		>
	</NavBrand>
	<NavHamburger />
	<NavUl>
		<NavLi style="font-size: 2em" href="{base}/">Home</NavLi>
		<NavLi style="font-size: 2em" href="{base}/music">Music</NavLi>
		<NavLi style="font-size: 2em" href="{base}/contact">Contact</NavLi>
	</NavUl>
</Navbar>
