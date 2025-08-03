<script lang="ts">
	//import { page } from "$app/state";
	//import GoogleModelViewer from '../components/GoogleModelViewer.svelte';
	//import { base } from "$app/paths";
	let name = 'Girly';
	let src = '$lib/../images/release_show_Large.jpeg';
</script>

<h1
	style="position:absolute; width:100%; top:calc(40vh); text-align: center; font-size: 5vh; color: white; text-shadow: 2px 2px 40px #38bdf8;font-family:Win95; font-weight:900; width: 100% z-index: 10;background-color: black;"
>
	We hit capacity. Thanks for Making it an Amazing Release Show!
</h1>
<img class="splash-img mx-auto my-auto" {src} alt="{name} dances." />
