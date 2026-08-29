<script lang="ts">
	import ShowDate from '$lib/components/ShowDate.svelte';
	import { base } from '$app/paths';

	// Sample show dates - replace with real data
	const upcomingShows = [		
		{
			date: 'September 12, 2026',
			time: '8:00 PM',
			venue: 'The Middle East (upstairs)',
			location: 'Cambridge, MA',
			additionalInfo: null,
			poster: '$lib/../images/middle_east_2026.jpg',
			ticketUrl: "https://www.ticketweb.com/event/fm-collective-the-funky-internationals-middle-east-upstairs-tickets/14291594?pl=mideastclub&REFID=clientsitewp"
		},
		{
			date: 'August 13, 2026',
			time: 'door: 7:00 PM, show: 8:00 PM',
			venue: 'Obrien\'s Pub',
			location: 'Allston, MA',
			additionalInfo: null,
			poster: '$lib/../images/obriens_2026.jpeg',
			ticketUrl: 'https://obrienspubboston.com/show/fae-feral-subcutaneous-sky-swallowed-girly-and-the-pops/'
		},
		{
			date: 'August 18, 2026',
			time: null,
			venue: 'The Fifth Column',
			location: 'Contact us for address',
			additionalInfo: null,
			poster: null,
			ticketUrl: null 
		}
	];

	const tours_2026 = [
		{
			date: 'July 31, 2026',
			time: null,
			venue: 'Getties',
			location: 'Providence, RI',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://www.bandsintown.com/t/108433722?came_from=2570&utm_medium=web&utm_source=artist_page&utm_campaign=ticket'
		},
		{
			date: 'August 06, 2026',
			time: 'door: 7:00 PM, show: 8:00 PM',
			venue: 'Cafe Nine',
			location: 'New Haven, CT',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://www.cafenine.com/products/events/girly-the-pops-radiodonta-royal-oaks-wolf-harbor-thursday-8-6-2026-8-00-pm-edt-53504121'
		},
		{
			date: 'August 08, 2026',
			time: 'door: 7:00 PM, show: 8:00 PM',
			venue: 'The Shrine',
			location: 'New York, NY',
			additionalInfo: 'free entry: 2271 Adam Clayton Powell Jr Blvd, New York, NY 10030',
			poster: null,
			ticketUrl: null
		},
		{
			date: 'August 12, 2026',
			time: null,
			venue: 'The Pocket',
			location: 'Washington, DC',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://app.opendate.io/e/the-garage-presents-girly-and-the-pops-costar-glass-island-sir-lando-august-12-2026-718744#tickets?click_id=Q5eICXfcQCatNPfr3-KYsw'
		},
		{
			date: 'August 13, 2026',
			time: null,
			venue: 'Abyssinia',
			location: 'Philadelphia, PA',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://www.eventbrite.com/e/eliza-claffy-the-breaks-and-girly-the-pops-run-for-the-hills-tour-dc-tickets-1992311315777?aff=aff0bandsintown&bit_userid=${user_id}&comeFrom=2570&artist_event_id=108433795#location'
		},
		{
			date: 'August 15, 2026',
			time: null,
			venue: 'Roboto',
			location: 'Pittsburgh, PA',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://tickets.venuepilot.com/e/girly-the-pops-2026-08-15-the-mr-roboto-project-pittsburgh-8c8659'
		},
		{
			date: 'August 19, 2026',
			time: null,
			venue: 'The Baby G',
			location: 'Toronto, ON',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://dice.fm/event/l8x29w-in-your-walls-g-string-sunniva-and-girly-and-the-pops-19th-aug-the-baby-g-toronto-tickets?pid=530cb286'
		},
		{
			date: 'August 20, 2026',
			time: null,
			venue: 'El Dorado',
			location: 'Troy, NY',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://www.eventbrite.com/e/ghost-prom-gas-leak-erie-girly-the-pops-live-at-el-dorado-tickets-1991104463048?aff=aff0bandsintown&bit_userid=%24%7Buser_id%7D&comeFrom=2570&artist_event_id=108437502'
		},
		{
			date: 'August 23, 2026',
			time: null,
			venue: 'Turbo Haüs',
			location: 'Montreal, QC',
			additionalInfo: null,
			poster: null,
			ticketUrl: 'https://thepointofsale.com/tickets/runfothehills?lang=en'
		},
		{
			date: 'August 27, 2026',
			time: null,
			venue: "Ralph's Rock Diner",
			location: 'Worcester, MA',
			additionalInfo: null,
			poster: null,
			ticketUrl: null
		},
	];

	const pastShows = [
		{
			date: 'August 28, 2026',
			time: null,
			venue: 'The Jungle',
			location: 'Boston, MA',
			additionalInfo: null,
			poster: '$lib/../images/release_2026.jpg',
			ticketUrl: 'https://www.eventbrite.com/checkout-external?eid=1994986385984'
		},
		{
			date: 'August 27, 2026',
			time: null,
			venue: "Ralph's Rock Diner",
			location: 'Worcester, MA',
			additionalInfo: null,
			poster: '$lib/../images/worcester_2026.jpg',
			ticketUrl: null
		},
		{
			date: 'August 23, 2026',
			time: null,
			venue: 'Turbo Haüs',
			location: 'Montreal, QC',
			additionalInfo: null,
			poster: '$lib/../images/turbo_haus_2026.jpg',
			ticketUrl: 'https://thepointofsale.com/tickets/runfothehills?lang=en'
		},
		{
			date: 'August 20, 2026',
			time: null,
			venue: 'El Dorado',
			location: 'Troy, NY',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://www.eventbrite.com/e/ghost-prom-gas-leak-erie-girly-the-pops-live-at-el-dorado-tickets-1991104463048?aff=aff0bandsintown&bit_userid=%24%7Buser_id%7D&comeFrom=2570&artist_event_id=108437502'
		},
		{
			date: 'August 19, 2026',
			time: null,
			venue: 'The Baby G',
			location: 'Toronto, ON',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://dice.fm/event/l8x29w-in-your-walls-g-string-sunniva-and-girly-and-the-pops-19th-aug-the-baby-g-toronto-tickets?pid=530cb286'
		},

		{
			date: 'August 15, 2026',
			time: null,
			venue: 'Roboto',
			location: 'Pittsburgh, PA',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://tickets.venuepilot.com/e/girly-the-pops-2026-08-15-the-mr-roboto-project-pittsburgh-8c8659'
		},
		{
			date: 'August 13, 2026',
			time: null,
			venue: 'Abyssinia',
			location: 'Philadelphia, PA',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://www.eventbrite.com/e/eliza-claffy-the-breaks-and-girly-the-pops-run-for-the-hills-tour-dc-tickets-1992311315777?aff=aff0bandsintown&bit_userid=${user_id}&comeFrom=2570&artist_event_id=108433795#location'
		},
		{
			date: 'August 12, 2026',
			time: null,
			venue: 'The Pocket',
			location: 'Washington, DC',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://app.opendate.io/e/the-garage-presents-girly-and-the-pops-costar-glass-island-sir-lando-august-12-2026-718744#tickets?click_id=Q5eICXfcQCatNPfr3-KYsw'
		},
		{
			date: 'August 08, 2026',
			time: 'door: 7:00 PM, show: 8:00 PM',
			venue: 'The Shrine',
			location: 'New York, NY',
			additionalInfo: 'free entry: 2271 Adam Clayton Powell Jr Blvd, New York, NY 10030',
			poster: null,
			ticketUrl: null
		},
		{
			date: 'August 06, 2026',
			time: 'door: 7:00 PM, show: 8:00 PM',
			venue: 'Cafe Nine',
			location: 'New Haven, CT',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://www.cafenine.com/products/events/girly-the-pops-radiodonta-royal-oaks-wolf-harbor-thursday-8-6-2026-8-00-pm-edt-53504121'
		},
		{
			date: 'July 31, 2026',
			time: null,
			venue: 'Getties',
			location: 'Providence, RI',
			additionalInfo: null,
			poster: null,
			ticketUrl:
				'https://www.bandsintown.com/t/108433722?came_from=2570&utm_medium=web&utm_source=artist_page&utm_campaign=ticket'
		},
		{
			date: 'July 11, 2026',
			time: '4:00 PM',
			venue: 'Long Live Roxbury',
			location: '52 Hampden St., Boston, MA',
			additionalInfo: 'Brewery',
			poster: null,
			ticketUrl: null
		},
		{
			date: 'July 11, 2026',
			time: '2:00 PM',
			venue: 'Block Party',
			location: 'Ridgemont St., Allston',
			additionalInfo: 'Allston Block Party',
			poster: null,
			ticketUrl: null
		},
		{
			date: 'June 25, 2026',
			time: '7:00 PM',
			venue: 'Cantab Lounge',
			location: 'Cambridge, MA',
			additionalInfo: null,
			poster: null,
			ticketUrl: null
		},
		{
			date: 'May 15, 2026',
			time: 'TBA',
			venue: 'Davis Square',
			location: 'Somerville, MA',
			additionalInfo: 'with Battlemode - details TBA',
			poster: '$lib/../images/down_in_davis.jpg',
			ticketUrl: null
		},
		{
			date: 'May 8, 2026',
			time: '7:00 PM',
			venue: 'Pasta Planet',
			location: 'DM for address',
			additionalInfo: null,
			poster: '$lib/../images/pasta_05_2026.jpg',
			ticketUrl: null
		},
		{
			date: 'May 6, 2026',
			time: '8:00 PM',
			venue: 'Silhouette Lounge',
			location: 'Allston, MA',
			additionalInfo: 'with Interzone and Saint Throwaway',
			poster: null,
			ticketUrl: null
		},
		{
			date: 'January 24, 2026',
			time: '8:00 PM',
			venue: 'Tourist Trap',
			poster: '$lib/../images/tt_01_26.jpg',
			location: 'DM for address',
			ticketUrl: 'door'
		},
		{
			date: 'January 23, 2026',
			time: '7:30 PM',
			venue: 'Rabies',
			location: 'DM for Address',
			poster: '$lib/../images/rabies_01_26.jpg',
			ticketUrl: 'door'
		},
		{
			date: 'January 23, 2026',
			time: '10:00 PM',
			venue: 'The Jungle',
			location: 'Union Square, Somerville, MA',
			poster:
				'https://img.evbuc.com/https%3A%2F%2Fcdn.evbuc.com%2Fimages%2F851425509%2F300850577841%2F1%2Foriginal.20240916-164052?crop=focalpoint&fit=crop&w=600&auto=format%2Ccompress&q=75&sharp=10&fp-x=0.502840909091&fp-y=0.56652360515&s=08e5661ab46112c0b54aff20aa9d7b4c',
			additionalInfo: '$15 @ door',
			ticketUrl: 'https://www.eventbrite.com/checkout-external?eid=1969919815196'
		},
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
	<section class="bg-grey mb-12 rounded-lg border-2" style="padding:15px">
		<h2 class="text-secondary-800 border-secondary-400 mb-6 border-b-2 pb-2 text-3xl font-bold">
			Upcoming Shows
		</h2>

		{#if upcomingShows.length > 0}
			<div
				class="space-y-4"
				style="background-color: rgba(0, 0, 0, 0.85); padding: 15px; border-radius: 8px;"
			>
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
			<div class="bg-grey rounded-lg p-8 text-center">
				<p class="text-secondary-700 text-xl">No upcoming shows scheduled yet. Check back soon!</p>
			</div>
		{/if}
	</section>
	<!-- Past Shows Section -->
	<section class="bg-grey rounded-lg border-2" style="padding:15px">
		<h2 class="text-secondary-800 border-secondary-400 mb-6 border-b-2 pb-2 text-3xl font-bold">
			Recent Shows
		</h2>

		{#if pastShows.length > 0}
			<div
				class="space-y-4"
				style="background-color: rgba(0, 0, 0, 0.85); padding: 15px; border-radius: 8px;"
			>
				{#each pastShows as show}
					<ShowDate
						date={show.date}
						time={show.time}
						venue={show.venue}
						location={show.location}
						additionalInfo={show.additionalInfo}
						posterUrl={show.poster}
					/>
				{/each}
			</div>
		{:else}
			<div class="bg-grey rounded-lg p-8 text-center opacity-75">
				<p class="text-secondary-700 text-xl">No past shows to display yet.</p>
			</div>
		{/if}
	</section>

	<!-- Tour 2026-->
	<!--- <section class="bg-grey mb-12 rounded-lg border-2" style="padding:15px; ">
		<h2 class="text-secondary-800 border-secondary-400 mb-6 border-b-2 pb-2 text-3xl font-bold">
			Tour 2026
		</h2>

		{#if tours_2026.length > 0}
			<div
				class="space-y-4"
				style="background-color: rgba(0, 0, 0, 0.85); padding: 15px; border-radius: 8px;"
			>
				{#each tours_2026 as show}
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
			<div class="bg-grey rounded-lg p-8 text-center">
				<p class="text-secondary-700 text-xl">No tour scheduled yet. Check back soon!</p>
			</div>
		{/if}
	</section> -->



	<!-- Contact for Booking -->
	<section class="mt-16 text-center">
		<div class="bg-secondary-100 border-secondary-300 rounded-lg border-2 p-8">
			<h3 class="text-secondary-800 mb-4 text-2xl font-bold">Book Us for Your Venue</h3>
			<p class="text-secondary-700 mb-4">
				Interested in having Girly and the Pops perform at your venue?
			</p>
			<a
				href="{base}/booking"
				class="bg-primary-500 hover:bg-primary-600 inline-block rounded-lg px-6 py-3 font-bold text-white transition-colors duration-200"
			>
				Contact Us
			</a>
		</div>
	</section>
</div>
