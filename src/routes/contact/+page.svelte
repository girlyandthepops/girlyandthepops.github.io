<script lang="ts">
	import axios from 'axios';
	import ContactForm from '$lib/components/ContactForm.svelte';
	let hasSubmit = $state(false);
	let setSubmitStateToTrue = () => {
		hasSubmit = true;
	};

	function submitToAPI(name: string, email: string, description: string) {
		const URL = 'https://7rtzb41rzc.execute-api.us-east-1.amazonaws.com/girlyandthepops';

		var data = JSON.stringify({
			name: name,
			email: email,
			description: description
		});
		let headers = {
			'Content-Type': 'application/json; charset=utf-8'
		};
		console.log('Submitting to API', data);
		axios
			.post(URL, data, { headers: headers })
			.then(function (response) {
				console.log(response);
			})
			.catch(function (error) {
				console.log('Error', error);
			});
		setSubmitStateToTrue();
	}
</script>

{#if hasSubmit === false} 
	<ContactForm submitHandler={submitToAPI} />
{:else}
<div class="bg-pink container mx-auto my-auto border-2 rounded-lg" style="width:min(80%,600px);padding:2em">
	<h3 class="text-decoration-thickness-4 text-center text-2xl" style="font-size: 3rem;">
		Thanks for contacting us! We'll get back to you soon 😉.
	</h3>
</div>
{/if}
