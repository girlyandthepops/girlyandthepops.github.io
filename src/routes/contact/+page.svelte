<script lang="ts">
	import axios from 'axios';
	import ContactForm from '$lib/components/ContactForm.svelte';
	let hasSubmit = $state(false);
	let setSubmitStateToTrue = () => {
		hasSubmit = true;
	};

	function submitToAPI(e) {
		e.preventDefault();
		const URL = 'https://7rtzb41rzc.execute-api.us-east-1.amazonaws.com/girlyandthepops';
		const name = document.getElementById('name');
		const email = document.getElementById('email');
		const description = document.getElementById('description');

		var data = JSON.stringify({
			name: name.value,
			email: email.value,
			description: description.value
		});
		let headers = {
			'Content-Type': 'application/json; charset=utf-8'
		};
		axios
			.post(URL, data, { headers: headers })
			.then(function (response) {
				console.log(response);
			})
			.catch(function (error) {
				console.log('Error', error);
			});
		name.value = '';
		email.value = '';
		description.value = '';
		setSubmitStateToTrue();
	}
</script>

{#if hasSubmit === false} 
	<ContactForm onsubmit={submitToAPI} />
{:else}
<div class="bg-pink container mx-auto my-auto" style="width:min(80%,600px);padding:2em">
	<h3 class="text-decoration-thickness-4 text-center text-2xl" style="font-size: 3rem;">
		Thanks for contacting us! We'll get back to you soon 😉.
	</h3>
</div>
{/if}
