<script lang="ts">
	import '../app.css'; // Sesuaikan jika Anda menggunakan metode CSS manual
	import Navbar from '$lib/components/Navbar.svelte';
	import Footer from '$lib/components/Footer.svelte'; // 1. Impor komponen Footer
</script>

<div class="flex min-h-screen flex-col bg-slate-50 font-sans">
	<Navbar />

	<main class="flex-grow">
		<slot />
	</main>

	<Footer /> </div>