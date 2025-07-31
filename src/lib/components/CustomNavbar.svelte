<script lang="ts">
	import { base } from '$app/paths';
	import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
</script>

<Navbar class="bg-pink" style="border-color:black; border-bottom-width:3px">
	<NavBrand href="{base}/">
		<img
			src="{base}/images/girly_in_action.png"
			style="height:30px;margin:10px;border-radius:20px"
			alt="Girly In Action"
		/>
		<span class="self-center text-xl font-semibold whitespace-nowrap dark:text-white"
			><h1>Girly & the Pops</h1></span
		>
	</NavBrand>
	<NavHamburger />
	<NavUl>
		<NavLi href="{base}/">Home</NavLi>
		<NavLi href="{base}/music">Music</NavLi>
		<NavLi href="{base}/contact">Contact</NavLi>
	</NavUl>
</Navbar>
