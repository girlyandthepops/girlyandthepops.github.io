<script lang="ts">
    //import { base } from "$app/paths";
    let name = 'Girly';
    let ep1 = '$lib/../images/ep/1.png';
    let ep2 = '$lib/../images/ep/2.png';
    let ep3 = '$lib/../images/ep/3.png';
    let ep4 = '$lib/../images/ep/4.png';
    let ep5 = '$lib/../images/ep/5.png';
    let ep6 = '$lib/../images/ep/6.png';
    let ep7 = '$lib/../images/ep/7.png';


    let src = '$lib/../images/ep/bacgrnd.png';
</script>
<div class="mx-auto" style="max-height:auto; display:flex">
    <img class="bg-pink ep-bg-img" src={src} alt="{name} lyrics."/>
    <div class="ep-container">
        <div class="tooltip" style="margin-top:19.5%">
            <img class="grow-and-rotate" src={ep1} alt="{name} lyrics."/>
            <img class="tooltipimgl" src="https://upload.wikimedia.org/wikipedia/commons/b/b6/Image_created_with_a_mobile_phone.png">
        </div>
        <div class="tooltip">
            <img class="grow-and-rotate" src={ep2} alt="{name} lyrics."/>
            <img class="tooltipimgr" src="https://upload.wikimedia.org/wikipedia/commons/b/b6/Image_created_with_a_mobile_phone.png">
        </div>
        <div class="tooltip">
            <img class="grow-and-rotate" src={ep3} alt="{name} lyrics."/>
            <img class="tooltipimgl" src="https://upload.wikimedia.org/wikipedia/commons/b/b6/Image_created_with_a_mobile_phone.png">
        </div>
        <div class="tooltip">
            <img class="grow-and-rotate" src={ep4} alt="{name} lyrics."/>
            <img class="tooltipimgr" src="https://upload.wikimedia.org/wikipedia/commons/b/b6/Image_created_with_a_mobile_phone.png">
        </div>
        <div class="tooltip">
            <img class="grow-and-rotate" src={ep5} alt="{name} lyrics."/>
            <img class="tooltipimgl" src="https://upload.wikimedia.org/wikipedia/commons/b/b6/Image_created_with_a_mobile_phone.png">
        </div>
        <div class="tooltip">
            <img class="grow-and-rotate" src={ep6} alt="{name} lyrics."/>
            <img class="tooltipimgr" src="https://upload.wikimedia.org/wikipedia/commons/b/b6/Image_created_with_a_mobile_phone.png">
        </div>
        <div class="tooltip">
            <img class="grow-and-rotate" src={ep7} alt="{name} lyrics."/>
            <img class="tooltipimgl" src="https://upload.wikimedia.org/wikipedia/commons/b/b6/Image_created_with_a_mobile_phone.png">
        </div>
    </div>
</div>
