<script lang="ts">
	import Music from '$lib/components/Music.svelte';
	import { base } from '$app/paths';
	let ggpops = '$lib/../images/epk/girlyandpopstext.png';
	let lucy = '$lib/../images/epk/lucyorb.gif';
	let mcfgcd = '$lib/../images/epk/MCFGCD.png';
	let mcfgtext = '$lib/../images/epk/MCFGtext.png';
	let live246cd = '$lib/../images/epk/LIVE246cd.png';
	let live246text = '$lib/../images/epk/LIVE246text.png';
	let bookingtext = '$lib/../images/epk/bookingtext.png';
	let mcfgImage: HTMLImageElement;
	let mcfgText: HTMLImageElement;
	let live246Image: HTMLImageElement;
	let live246Text: HTMLImageElement;
	let bookingText: HTMLImageElement;
	let ggpopsImage: HTMLImageElement;
	let lucyImage: HTMLImageElement;


	let handleImageEnter = (event: MouseEvent) => {
		lucyImage.style.cursor = 'pointer';
		lucyImage.style.filter = 'invert()';
	};
	let handleImageLeave = (event: MouseEvent) => {
		lucyImage.style.cursor = 'default';
		lucyImage.style.filter = 'saturate(100%)';
	};
	let handlelive246Enter = (event: MouseEvent) => {
		live246Image.style.animation = 'spin 2s linear infinite';
		live246Text.style.animation = 'spin-counter 4s linear infinite';
		live246Image.style.cursor = 'pointer';
	};

	let handlelive246Leave = (event: MouseEvent) => {
		live246Image.style.animation = '';
		live246Text.style.animation = '';
	};

	let handleMCFGEnter = (event: MouseEvent) => {
		mcfgImage.style.animation = 'spin 2s linear infinite';
		mcfgText.style.animation = 'spin-counter 4s linear infinite';
		mcfgImage.style.cursor = 'pointer';
	};

	let handleMCFGLeave = (event: MouseEvent) => {
		mcfgImage.style.animation = '';
		mcfgText.style.animation = '';
	};
	let handleBookingEnter = (event: MouseEvent) => {
		bookingText.style.animation = 'growAndRotate 0.2s linear infinite';
		bookingText.style.cursor = 'pointer';
	};
	let handleBookingLeave = (event: MouseEvent) => {
		bookingText.style.animation = '';
	};
</script>

<div
	class="bg-grey shadow-2xl"
	style="position:relative;margin-bottom:2em;padding:0;margin:auto;width:min(80vw,52vh);aspect-ratio:2334 / 3300;background-image:url('$lib/../images/epk/epk_background.jpeg');background-size:100% 100%"
>
	<img
		bind:this={lucyImage}
		style="position:absolute;top:12%;left:20%;width:60%;aspect-ratio:1 / 1;"
		src={lucy}
		on:mouseleave={handleImageLeave}
		on:mouseenter={handleImageEnter}
		on:click={()=>{window.open('https://www.youtube.com/watch?v=sxxxcswQ4fY', '_blank', 'noopener,noreferrer');}}
	/>
	<img
		bind:this={ggpopsImage}
		style="position:absolute;top:0;left:0;pointer-events:none;"
		src={ggpops}
	/>
	<img
		bind:this={mcfgImage}
		class="grow-and-rotate"
		style="position:absolute;top:51.25%;left:73.5%;width:22%"
		src={mcfgcd}
		on:mouseenter={handleMCFGEnter}
		on:mouseleave={handleMCFGLeave}
		on:click={()=>{window.location.href = '/music';}}
	/>
	<img
		bind:this={mcfgText}
		class="grow-and-rotate"
		style="position:absolute;top:49.75%;left:71%;pointer-events:none;width:27%"
		src={mcfgtext}
	/>
	<img
		bind:this={live246Image}
		class="grow-and-rotate"
		style="position:absolute;top:64%;left:5.5%;width:23%"
		src={live246cd}
		on:mouseenter={handlelive246Enter}
		on:mouseleave={handlelive246Leave}
		on:click={()=>{window.location.href = '/music';}}
	/>
	<img
		bind:this={live246Text}
		class="grow-and-rotate"
		style="position:absolute;top:62.5%;pointer-events:none;left:3.5%;;width:27%"
		src={live246text}
	/>
	<img
		bind:this={bookingText}
		class="grow-and-rotate"
		style="position:absolute;top:65%;left:26.75%;width:55%;rotate:30deg;"
		src={bookingtext}
		on:mouseenter={handleBookingEnter}
		on:mouseleave={handleBookingLeave}
		on:click={()=>{window.location.href = '/booking';}}
	/>
	<p
		style="position:absolute;bottom:0;left:0;pointer-events:none;padding:5%;color:#dcd2d1;font-size:min(1.6vw,1vh)"
	>
		Based in Boston Girly and the Pops is the synthesis of 4 misfits* contexts, influences and
		emotions. Songs move freely from 2000s garage rock to reggaeton and anywhere in between. The
		music is honest, urgent and free: spoken verses turn from belts to screams.complex and playful
		pockets blur the lines of genre, as precise riffs cut through swaying basslines. Having released
		two EPs since their formation in Fall 2024. they are now writing their debut LP set for release
		summer of 2026.
	</p>
</div>
