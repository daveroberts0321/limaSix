<script>
	import ImageGallery from '$lib/components/ImageGallery.svelte';
	import ProductInfo from '$lib/components/ProductInfo.svelte';
	import EmailSignup from '$lib/components/EmailSignup.svelte';
	import SocialLinks from '$lib/components/SocialLinks.svelte';
</script>

<svelte:head>
	<title>Innovative Sports Equipment - Coming Soon</title>
	<meta name="description" content="Discover our revolutionary sports equipment. Sign up for updates on our patent-pending innovation." />
</svelte:head>

<main class="min-h-screen bg-gray-50 py-12">
	<div class="container mx-auto px-4">
		<ImageGallery />
		<ProductInfo />
		<EmailSignup />
		<SocialLinks />
	</div>
</main>

<style>
	:global(html) {
		scroll-behavior: smooth;
	}
</style>