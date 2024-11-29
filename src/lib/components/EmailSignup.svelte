<script>
	let email = '';
	let submitted = false;
	let error = '';

	async function handleSubmit() {
		if (!email) {
			error = 'Please enter your email address';
			return;
		}

		// Here you would typically send this to your backend
		// For now, we'll just simulate success
		submitted = true;
		error = '';
	}
</script>

<div class="max-w-2xl mx-auto px-4 py-12 bg-gray-50 rounded-lg mt-12">
	<h2 class="text-2xl font-bold text-center mb-4">Stay Updated</h2>
	<p class="text-center text-gray-600 mb-6">
		Join our mailing list to receive updates about our product launch and exclusive offers.
	</p>

	{#if submitted}
		<div class="text-center p-4 bg-green-100 text-green-700 rounded-lg">
			Thank you for signing up! We'll keep you posted on our latest updates.
		</div>
	{:else}
		<form on:submit|preventDefault={handleSubmit} class="space-y-4">
			<div>
				<input
					type="email"
					bind:value={email}
					placeholder="Enter your email address"
					class="w-full px-4 py-2 rounded-lg border-gray-300 focus:ring-primary focus:border-primary"
				/>
				{#if error}
					<p class="text-red-500 text-sm mt-1">{error}</p>
				{/if}
			</div>
			<button
				type="submit"
				class="w-full bg-primary text-white py-2 px-4 rounded-lg hover:bg-secondary transition-colors"
			>
				Sign Up for Updates
			</button>
		</form>
	{/if}
</div>