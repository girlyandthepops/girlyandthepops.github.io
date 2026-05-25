<script lang="ts">
	let {
		date,
		location,
		time,
		venue,
		ticketUrl = null,
		additionalInfo = null,
		posterUrl = null
	} = $props();
</script>

<div class="show-date-card bg-grey border-secondary-400 mb-4 rounded-lg border-2 p-4 shadow-md">
	<div class="flex flex-col md:flex-row md:items-center md:justify-between">
		<div class="flex-1">
			<h3 class="text-secondary-800 mb-2 text-xl font-bold">{venue}</h3>
			<p class="text-secondary-700 mb-1">{location}</p>
			<div class="flex flex-col sm:flex-row sm:items-center sm:gap-4">
				<p class="text-secondary-600 font-semibold">{date}</p>
				<p class="text-secondary-600">{time}</p>
				{#if additionalInfo}
					<p class="text-secondary-600">{additionalInfo}</p>
				{/if}
			</div>
			{#if posterUrl}
				<a href={posterUrl} target="_blank" rel="noopener noreferrer">
					<img
						src={posterUrl}
						alt="Poster for {venue}"
						class="mt-2 max-h-48 w-auto rounded-lg shadow-md"
					/>
				</a>
			{/if}
		</div>
		<div class="mt-3 md:mt-0">
			{#if ticketUrl}
				{#if ticketUrl === 'door'}
					<span
						class="inline-block cursor-not-allowed rounded bg-gray-400 px-4 py-2 font-bold text-white"
					>
						At Door
					</span>
				{:else}
					<a
						href={ticketUrl}
						class="bg-secondary-500 hover:bg-secondary-600 inline-block rounded px-4 py-2 font-bold text-white transition-colors duration-200"
						target="_blank"
						rel="noopener noreferrer"
					>
						Get Tickets
					</a>
				{/if}
			{/if}
		</div>
	</div>
</div>
