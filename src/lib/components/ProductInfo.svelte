<script>
	export let title = "MAKING BELT FEDS AFFORDABLE";
	export let subtitle = "Patent Pending Innovation";
	export let description = `
		Our mission is to make belt feds affordable to working class patriots. The LIMA SIX is an affordable, reliable belt fed upper receiver for your AR15. But we aren’t just about being the cheapest on the block. Here is what sets the LIMA SIX apart from the competition:
	`;
	export let features = [
		"23% more bolt carrier travel than an AR15 (Patent Pending)",
		"Constant recoil design makes full auto firing more controllable",
		"Increased reliability stripping rounds from links",
		"Dual ejectors for increased reliability and parts life",
    "Parts compatibility with many AR15 parts, barrels, GasBlock, Handguard"
  ];	
</script>

<div class="max-w-4xl mx-auto px-4 py-8">
	<h1 class="text-4xl font-bold text-center mb-2">{title}</h1>
	<h2 class="text-xl text-gray-600 text-center mb-8">{subtitle}</h2>
	
	<p class="text-lg text-gray-700 mb-8 leading-relaxed">
		{description}
	</p>
	
	<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
		{#each features as feature}
			<div class="bg-white p-4 rounded-lg shadow-md">
				<div class="flex items-center">
					<svg class="w-6 h-6 text-primary mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
						<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
					</svg>
					<span class="text-gray-800">{feature}</span>
				</div>
			</div>
		{/each}
	</div>
</div>