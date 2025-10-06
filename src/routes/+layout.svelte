<script lang="ts">
	import Navbar from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import { afterNavigate } from '$app/navigation';

	// Kirim event page_view ke Google Analytics setiap kali halaman berpindah
	afterNavigate(() => {
		if (window.gtag) {
			window.gtag('event', 'page_view', {
				page_path: window.location.pathname,
				page_title: document.title
			});
		}
	});
</script>

<svelte:head>
	<!-- Google tag (gtag.js) -->
	<script async src="https://www.googletagmanager.com/gtag/js?id=G-V210RTREDN"></script>
	<script>
		window.dataLayer = window.dataLayer || [];
		function gtag(){dataLayer.push(arguments);}
		gtag('js', new Date());
		gtag('config', 'G-V210RTREDN');
	</script>
</svelte:head>

<div class="flex min-h-screen flex-col bg-slate-50 font-sans">
	<Navbar />

	<main class="flex-grow">
		<slot />
	</main>

	<Footer />
</div>
