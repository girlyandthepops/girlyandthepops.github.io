<script lang="ts">
	import ShowDate from '$lib/components/ShowDate.svelte';
	import { base } from '$app/paths';

	// Sample show dates - replace with real data
	const upcomingShows = [
				{
			date: 'January 23, 2026',
			time: '8:00 PM',
			venue: 'The Jungle',
			location: 'Union Square, Somerville, MA',
			poster: "https://img.evbuc.com/https%3A%2F%2Fcdn.evbuc.com%2Fimages%2F851425509%2F300850577841%2F1%2Foriginal.20240916-164052?crop=focalpoint&fit=crop&w=600&auto=format%2Ccompress&q=75&sharp=10&fp-x=0.502840909091&fp-y=0.56652360515&s=08e5661ab46112c0b54aff20aa9d7b4c",
			additionalInfo: '$15 @ door',
			ticketUrl: 'https://www.eventbrite.com/checkout-external?eid=1969919815196'
		},
		{
			date: 'January 24, 2026',
			time: '8:00 PM',
			venue: 'Tourist Trap',
			poster: 'https://scontent-bos5-1.cdninstagram.com/v/t51.82787-15/616288069_17937434775128959_6492317695885235527_n.webp?_nc_cat=109&ig_cache_key=MzgwOTIzMjg3OTQyODM3NzUxNA%3D%3D.3-ccb7-5&ccb=7-5&_nc_sid=58cdad&efg=eyJ2ZW5jb2RlX3RhZyI6InhwaWRzLjExNTJ4MTQ0MC5zZHIuQzMifQ%3D%3D&_nc_ohc=7cvKFgQz6qgQ7kNvwF-4anu&_nc_oc=AdmpVWG3JYkmYKguIFML1ycZvLs_36Y0OqPz-_YrBO5QCGKi3NqJEt2Z6tGoiT8sMw4&_nc_ad=z-m&_nc_cid=0&_nc_zt=23&_nc_ht=scontent-bos5-1.cdninstagram.com&_nc_gid=5ZbaLUvKwIa-tp257T0TjA&oh=00_AfqrIgCUo9OhzQ8kKIWpFAXQyHDjUaekseQ9c-lMtOfW8A&oe=696ED191',
			location: 'DM for address',
			ticketUrl: 'door'
		},
	];

	const pastShows = [
		{
			date: 'December 13, 2025',
			time: '9:00 PM',
			venue: 'The Jungle',
			location: 'Union Square, Somerville, MA',
			ticketUrl: 'door'
		},
		{
			date: 'December 13, 2025',
			time: '3:00 PM',
			venue: 'School House',
			location: 'DM for address',
			ticketUrl: 'door'
		},
		{
			date: 'December 5, 2025',
			time: '9:00 PM',
			venue: 'The Jungle',
			location: 'Union Square, Somerville, MA',
			ticketUrl: 'door'
		},
		{
			date: 'November 28, 2025',
			time: '8:00 PM',
			venue: 'Pasta Planet',
			location: 'DM for address',
			ticketUrl: 'door'
		},
		{
			date: 'November 4, 2025',
			time: '10:00 PM',
			venue: 'The Jungle',
			location: 'Union Square, Somerville, MA',
			ticketUrl: 'door'
		},
		{
			date: 'October 10, 2025',
			time: '7:30 PM',
			venue: 'The Jungle',
			location: 'Union Square, Somerville, MA',
			ticketUrl: 'door' // Sold out
		},
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
						additionalInfo={show.additionalInfo}
						posterUrl={show.poster}
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
