<script lang="ts">
    import { base } from '$app/paths';
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from "flowbite-svelte";
</script>

<Navbar style="height:7vh;" class="bg-pink">
  <NavBrand href="{base}/">
    <img src="{base}/images/girly_in_action.png" class="me-3 h-6 sm:h-9" alt="Girly In Action" />
    <span class="self-center text-xl font-semibold whitespace-nowrap dark:text-white">Girly & the Pops</span>
  </NavBrand>
  <NavHamburger />
  <NavUl>
    <NavLi href="{base}/">Home</NavLi>
    <NavLi href="{base}/music">Music</NavLi>
    <NavLi href="{base}/shows">Shows</NavLi>
    <NavLi href="{base}/contact">Contact</NavLi>
  </NavUl>
</Navbar>
<hr style="border-top: 3px solid #000000" />

