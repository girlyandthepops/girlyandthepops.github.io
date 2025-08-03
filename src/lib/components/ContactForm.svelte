<script lang="ts">
    let {onsubmit} = $props();
</script>

<div
	id="contact"
	class="bg-pink container mx-auto my-auto"
	style="width:min(80%,600px);padding:2em"
>
	<div class="container">
		<h3 class="text-decoration-thickness-4 text-center text-2xl underline" style="font-size: 3rem;">
			Contact and Booking
		</h3>
		<div style="display:flex; flex-direction:column; align-items:center; justify-content:center;">
			<div class="p-7" style="width:100%">
				<form onsubmit={onsubmit}>
					<div class="form-group">
						<input
							class="form-control px-7"
							style="width:100%"
							id="name"
							name="name"
							placeholder="Name"
							type="text"
							required
						/>
					</div>
					<div class="form-group">
						<input
							class="form-control mt-4 px-7"
							style="width:100%"
							id="email"
							name="email"
							placeholder="Email"
							type="email"
							required
						/>
					</div>
					<div>
						<textarea
							class="form-control mt-4"
							style="width:100%"
							id="description"
							name="description"
							placeholder="Description"
							rows="5"
						></textarea>
					</div>
					<br />
					<button
						type="submit"
						class="bg-secondary-400 me-2 mb-2 rounded-full px-5 py-2.5 text-center font-medium text-white hover:bg-blue-500 focus:ring-4 focus:ring-blue-300 focus:outline-none"
						style="width:100%">submit</button
					>
				</form>
			</div>
		</div>
		<hr />
		<h3 class="text-decoration-thickness-4 text-center text-2xl underline" style="font-size: 3rem;">
			Send us an email:
		</h3>
		<div class="tab-content">
			<p><span class="glyphicon glyphicon-envelope"></span>Email: girlyandthepops@gmail.com</p>
		</div>
	</div>
</div>
