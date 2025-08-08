<script lang="ts">
	import '../app.css'; // Sesuaikan dengan setup CSS Anda
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