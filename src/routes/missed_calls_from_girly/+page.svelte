<script lang="ts">
	import Untitled01 from '$lib/components/Lyrics/Untitled01.svelte';
	import Mazes from '$lib/components/Lyrics/Mazes.svelte';
	import EvilStreet from '$lib/components/Lyrics/EvilStreet.svelte';
	import Veil from '$lib/components/Lyrics/Veil.svelte';
	import Louie from '$lib/components/Lyrics/Louie.svelte';
	import SholdveCried from '$lib/components/Lyrics/SholdveCried.svelte';
	import HuntingHill from '$lib/components/Lyrics/HuntingHill.svelte';

	let ep1 = '$lib/../images/ep/1.png';
	let ep2 = '$lib/../images/ep/2.png';
	let ep3 = '$lib/../images/ep/3.png';
	let ep4 = '$lib/../images/ep/4.png';
	let ep5 = '$lib/../images/ep/5.png';
	let ep6 = '$lib/../images/ep/6.png';
	let ep7 = '$lib/../images/ep/7.png';


	let child = $state(Untitled01);

	let lyricsvisible = $state(false);
	let setlyricsvisible = (visible: boolean) => {
		lyricsvisible = visible;
	};
	let src = '$lib/../images/ep/bacgrnd.png';

	import LyricSheet from '$lib/components/LyricSheet.svelte';
</script>

<div style="margin: auto; display:flex; flex-direction:column;overflow-y:hidden">
	<div class="ep-container">
		<img class="bg-pink ep-bg-img" {src} alt="Missed calls from Girly lyrics." />
		<div class="tooltip" style="margin-top:19.5%">
			<img
				class="grow-and-rotate"
				src={ep1}
				alt="Untitled 01"
				onclick={() => {
					setlyricsvisible(true);
					child = Untitled01;
				}}
			/>
			<LyricSheet customClass="tooltipimgl" visible={true} closeHandler={() => {}}
				><Untitled01 /></LyricSheet
			>
		</div>
		<div class="tooltip">
			<img
				class="grow-and-rotate"
				src={ep2}
				alt="Mazes"
				onclick={() => {
					setlyricsvisible(true);
					child = Mazes;
				}}
			/>
			<LyricSheet customClass="tooltipimgr" visible={true} closeHandler={() => {}}
				><Mazes /></LyricSheet
			>
		</div>
		<div class="tooltip">
			<img
				class="grow-and-rotate"
				src={ep3}
				alt="Evil Street"
				onclick={() => {
					setlyricsvisible(true);
					child = EvilStreet;
				}}
			/>
			<LyricSheet customClass="tooltipimgl" visible={true} closeHandler={() => {}}
				><EvilStreet /></LyricSheet
			>
		</div>
		<div class="tooltip">
			<img
				class="grow-and-rotate"
				src={ep4}
				alt="Veil"
				onclick={() => {
					setlyricsvisible(true);
					child = Veil;
				}}
			/>
			<LyricSheet customClass="tooltipimgr" visible={true} closeHandler={() => {}}
				><Veil /></LyricSheet
			>
		</div>
		<div class="tooltip">
			<img
				class="grow-and-rotate"
				src={ep5}
				alt="Louie"
				onclick={() => {
					setlyricsvisible(true);
					child = Louie;
				}}
			/>
			<LyricSheet customClass="tooltipimgl" visible={true} closeHandler={() => {}}
				><Louie /></LyricSheet
			>
		</div>
		<div class="tooltip">
			<img
				class="grow-and-rotate"
				src={ep6}
				alt="Should've Cried"
				onclick={() => {
					setlyricsvisible(true);
					child = SholdveCried;
				}}
			/>
			<LyricSheet customClass="tooltipimgr" visible={true} closeHandler={() => {}}
				><SholdveCried /></LyricSheet
			>
		</div>
		<div class="tooltip">
			<img
				class="grow-and-rotate"
				src={ep7}
				alt="Hunting Hill"
				onclick={() => {
					setlyricsvisible(true);
					child = HuntingHill;
				}}
			/>
			<LyricSheet customClass="tooltipimgl" visible={true} closeHandler={() => {}}
				><HuntingHill /></LyricSheet
			>
		</div>
		{#if lyricsvisible}
			<LyricSheet customClass="lyric-sheet" visible={true} closeHandler={setlyricsvisible}
				>{@render child()}</LyricSheet
			>
		{/if}
	</div>
</div>
