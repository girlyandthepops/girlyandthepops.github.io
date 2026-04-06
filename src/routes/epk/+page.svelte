<script lang="ts">
	import Music from '$lib/components/Music.svelte';
	import { base } from '$app/paths';
	let booking= '$lib/../images/booking.png';
	let ggpops = '$lib/../images/girly_and_the_pops.png';
	let lucy = '$lib/../images/lucyorb.gif';
	let music = '$lib/../images/music.png';
	let music_titles = '$lib/../images/music_titles.png';
	let bookingImage: HTMLImageElement;
	let ggpopsImage: HTMLImageElement;
	let musicImage: HTMLImageElement;
	let lucyImage: HTMLImageElement;


	function isOpaqueAtPoint(image: HTMLImageElement, event: MouseEvent) {
		if (!image.complete || !image.naturalWidth || !image.naturalHeight) return;

		const rect = image.getBoundingClientRect();
		if (!rect.width || !rect.height) return;
		if (
			event.clientX < rect.left ||
			event.clientX > rect.right ||
			event.clientY < rect.top ||
			event.clientY > rect.bottom
		) {
			return false;
		}

		const scaleX = image.naturalWidth / rect.width;
		const scaleY = image.naturalHeight / rect.height;
		const x = Math.max(0, Math.min(image.naturalWidth - 1, Math.floor((event.clientX - rect.left) * scaleX)));
		const y = Math.max(0, Math.min(image.naturalHeight - 1, Math.floor((event.clientY - rect.top) * scaleY)));

		const canvas = document.createElement('canvas');
		canvas.width = image.naturalWidth;
		canvas.height = image.naturalHeight;

		const context = canvas.getContext('2d');
		if (!context) return;

		context.drawImage(image, 0, 0);
		const [, , , alpha] = context.getImageData(x, y, 1, 1).data;

		return alpha > 0;
	}

	function handleImageClick(event: MouseEvent) {
		if (bookingImage && isOpaqueAtPoint(bookingImage, event)) {
			window.location.href = '/contact';
			return;
		}else if (musicImage && isOpaqueAtPoint(musicImage, event)) {
			window.location.href = '/music';
		}else if (ggpopsImage && isOpaqueAtPoint(ggpopsImage, event)) {
			window.location.href = '/';
		}else if (lucyImage && isOpaqueAtPoint(lucyImage, event)) {
			window.open('https://www.youtube.com/watch?v=sxxxcswQ4fY', '_blank', 'noopener,noreferrer');
		}
	}

</script>

<div
	class="bg-pink shadow-2xl"
	style="position:relative;margin-bottom:2em;padding:0;margin:auto;width:min(800px,80vw);aspect-ratio:2334 / 3300;background-image:url('$lib/../images/epk_background.jpeg');background-size:100% 100%"
	on:click={handleImageClick}
>
<img
	bind:this={lucyImage}
	class="grow-and-rotate"
	style="position:absolute;top:12%;left:20%;width:60%;aspect-ratio:1 / 1;pointer-events:none;"
	src={lucy}
/>
<img
	bind:this={ggpopsImage}
	class="grow-and-rotate"
	style="position:absolute;top:0;left:0;pointer-events:none;"
	src={ggpops}
/>
<img
	bind:this={musicImage}
	class="grow-and-rotate"
	style="position:absolute;top:0;left:0;pointer-events:none;"
	src={music}
/>
<img
	class="grow-and-rotate"
	style="position:absolute;top:0;left:0;pointer-events:none;"
	src={music_titles}
/>
<img
	bind:this={bookingImage}
	class="grow-and-rotate"
	style="position:absolute;top:0;left:0;pointer-events:none;"
	src={booking}
/>
<p style="position:absolute;bottom:0;left:0;pointer-events:none;padding:5%;color:#dcd2d1;font-size:min(16px,1.6vw)">
Based in Boston Girly and the Pops is the synthesis of 4 misfits* contexts, influences and emotions. Songs move freely from 2000s garage rock to reggaeton and anywhere in between. The music is honest, urgent and free: spoken verses turn from belts to screams.complex and playful pockets blur the lines of genre, as precise riffs cut through swaying basslines. Having released two EPs since their formation in Fall 2024. they are now writing their debut LP set for release summer of 2026.
</p>
</div>
