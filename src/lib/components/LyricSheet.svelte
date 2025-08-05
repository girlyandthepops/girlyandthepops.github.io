<script lang="ts">
    let { children, visible, customClass, closeHandler } =  $props();
    let isvisible= $state(visible);
    let setIsVisible = (visible: boolean) => {
        isvisible = visible;
    };
</script>

<div class={customClass} style="display:{isvisible ? 'flex' : 'none'}">
	<button
		style="font-family:Win95;position:absolute;top:3px;right:10px"
		onclick={() => {
			//document.querySelector('#lyric-sheet').style.display = 'none';
            closeHandler(false);
		}}>close X</button
	>
    {@render children()}
</div>
