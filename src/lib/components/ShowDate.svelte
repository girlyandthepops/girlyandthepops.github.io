<script lang="ts">
    let { date, location, time, venue, ticketUrl = null } = $props();
</script>

<div class="show-date-card bg-pink p-4 mb-4 rounded-lg shadow-md border-2 border-secondary-400">
    <div class="flex flex-col md:flex-row md:items-center md:justify-between">
        <div class="flex-1">
            <h3 class="text-xl font-bold text-secondary-800 mb-2">{venue}</h3>
            <p class="text-secondary-700 mb-1">{location}</p>
            <div class="flex flex-col sm:flex-row sm:items-center sm:gap-4">
                <p class="text-secondary-600 font-semibold">{date}</p>
                <p class="text-secondary-600">{time}</p>
            </div>
        </div>
        <div class="mt-3 md:mt-0">
            {#if ticketUrl}
                {#if ticketUrl === "door"}
                    <span class="inline-block bg-gray-400 text-white font-bold py-2 px-4 rounded cursor-not-allowed">
                        At Door
                    </span>
                {:else}
                <a 
                    href={ticketUrl} 
                    class="inline-block bg-secondary-500 hover:bg-secondary-600 text-white font-bold py-2 px-4 rounded transition-colors duration-200"
                    target="_blank" 
                    rel="noopener noreferrer"
                >
                    Get Tickets
                </a>
                {/if}
            {:else}
                <span class="inline-block bg-gray-400 text-white font-bold py-2 px-4 rounded cursor-not-allowed">
                    Sold Out
                </span>
            {/if}
        </div>
    </div>
</div>
