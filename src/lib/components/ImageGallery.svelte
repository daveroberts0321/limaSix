<script>
	export let images = [
		{
			src: '/images/main.jpg',
			alt: 'Product Image 1',
			caption: 'Front view of the product'
		},
		{
			src: '/images/image2.jpg',
			alt: 'Product Image 2',
			caption: 'Side view showing unique features'
		},
		{
			src: '/images/image3.jpg',
			alt: 'Product Image 3',
			caption: 'Product in action'
		}
	];

	let currentIndex = 0;

	function nextImage() {
		currentIndex = (currentIndex + 1) % images.length;
	}

	function previousImage() {
		currentIndex = (currentIndex - 1 + images.length) % images.length;
	}
</script>

<div class="relative w-full max-w-4xl mx-auto">
	<div class="aspect-w-16 aspect-h-9 bg-gray-100 rounded-lg overflow-hidden">
		<img
			src={images[currentIndex].src}
			alt={images[currentIndex].alt}
			class="w-full h-full object-cover"
		/>
	</div>
	
	<div class="absolute inset-0 flex items-center justify-between p-4">
		<button
			on:click={previousImage}
			class="bg-black bg-opacity-50 text-white p-2 rounded-full hover:bg-opacity-75"
		>
			←
		</button>
		<button
			on:click={nextImage}
			class="bg-black bg-opacity-50 text-white p-2 rounded-full hover:bg-opacity-75"
		>
			→
		</button>
	</div>
	
	<p class="text-center mt-2 text-gray-600">{images[currentIndex].caption}</p>
</div>