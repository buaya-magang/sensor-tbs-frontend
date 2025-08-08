<script lang="ts">
	// Hapus 'import ../app.css' dari sini
	import Navbar from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte';
</script>

<div class="flex min-h-screen flex-col bg-slate-50 font-sans">
	<Navbar />

	<main class="flex-grow">
		<slot />
	</main>

	<Footer />
</div>