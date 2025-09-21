<script lang="ts">
	import ShowDate from '$lib/components/ShowDate.svelte';
	import { base } from '$app/paths';

	// Sample show dates - replace with real data
	const upcomingShows = [
		{
			date: 'October 10, 2025',
			time: '7:30 PM',
			venue: 'The Jungle',
			location: 'Union Square, Somerville, MA',
			ticketUrl: 'door' // Sold out
		}
	];

	const pastShows = [
		{
			date: 'September 20, 2025',
			time: '9:00 PM',
			venue: 'The Glue Factory',
			location: 'DM for address',
			ticketUrl: 'door'
		},
		{
			date: 'September 18, 2025',
			time: '9:00 PM',
			venue: 'The Jungle',
			location: 'Union Square, Somerville, MA',
			ticketUrl: 'door'
		},
		{
			date: 'September 6, 2025',
			time: '9:00 PM',
			venue: 'The Cantab Lounge Underground',
			location: 'Central Square, Cambridge, MA',
			ticketUrl: 'door'
		},
		{
			date: 'August 30, 2025',
			time: '8:00 PM',
			venue: 'The Midway Cafe',
			location: 'Jamaica Plain, MA',
			ticketUrl: 'https://www.facebook.com/events/692645947152327/'
		},
		{
			date: 'August 1, 2025',
			time: '7:00 PM',
			venue: 'Pasta Planet',
			location: 'DM for address',
			ticketUrl: null
		}
	];
</script>

<svelte:head>
	<title>Shows - Girly and the Pops</title>
	<meta name="description" content="Upcoming and past shows for Girly and the Pops" />
</svelte:head>

<div class="container mx-auto max-w-4xl px-4 py-8">
	<div class="bg-primary-200 mb-12 rounded-lg border-2 text-center" style="padding:15px">
		<h1
			class="text-secondary-800 mb-4 text-4xl font-bold md:text-6xl"
			style="font-family: Win95;text-decoration: underline;"
		>
			SHOW DATES
		</h1>
		<p class="text-secondary-600 mb-6 text-lg">
			Come see Girly and the Pops live! Check out our upcoming shows and get your tickets.
		</p>
	</div>

	<!-- Upcoming Shows Section -->
	<section class="bg-primary-200 mb-12 rounded-lg border-2" style="padding:15px">
		<h2
			class="text-secondary-800 border-secondary-400 mb-6 border-b-2 pb-2 text-3xl font-bold"
			style="font-family: Win95;"
		>
			Upcoming Shows
		</h2>

		{#if upcomingShows.length > 0}
			<div class="space-y-4">
				{#each upcomingShows as show}
					<ShowDate
						date={show.date}
						time={show.time}
						venue={show.venue}
						location={show.location}
						ticketUrl={show.ticketUrl}
					/>
				{/each}
			</div>
		{:else}
			<div class="bg-pink rounded-lg p-8 text-center">
				<p class="text-secondary-700 text-xl" style="font-family: Win95;">
					No upcoming shows scheduled yet. Check back soon!
				</p>
			</div>
		{/if}
	</section>

	<!-- Past Shows Section -->
	<section class="bg-primary-200 rounded-lg border-2" style="padding:15px">
		<h2
			class="text-secondary-800 border-secondary-400 mb-6 border-b-2 pb-2 text-3xl font-bold"
			style="font-family: Win95;"
		>
			Recent Shows
		</h2>

		{#if pastShows.length > 0}
			<div class="space-y-4 opacity-75">
				{#each pastShows as show}
					<ShowDate
						date={show.date}
						time={show.time}
						venue={show.venue}
						location={show.location}
						ticketUrl={show.ticketUrl}
					/>
				{/each}
			</div>
		{:else}
			<div class="bg-pink rounded-lg p-8 text-center opacity-75">
				<p class="text-secondary-700 text-xl" style="font-family: Win95;">
					No past shows to display yet.
				</p>
			</div>
		{/if}
	</section>

	<!-- Contact for Booking -->
	<section class="mt-16 text-center">
		<div class="bg-secondary-100 border-secondary-300 rounded-lg border-2 p-8">
			<h3 class="text-secondary-800 mb-4 text-2xl font-bold" style="font-family: Win95;">
				Book Us for Your Venue
			</h3>
			<p class="text-secondary-700 mb-4">
				Interested in having Girly and the Pops perform at your venue?
			</p>
			<a
				href="{base}/contact"
				class="bg-primary-500 hover:bg-primary-600 inline-block rounded-lg px-6 py-3 font-bold text-white transition-colors duration-200"
				style="font-family: Win95;"
			>
				Contact Us
			</a>
		</div>
	</section>
</div>
