<script lang="ts">
	import '../app.css'; // Import file CSS utama untuk Tailwind
	import Navbar from '$lib/components/Navbar.svelte';
</script>

<div class="min-h-screen bg-slate-50 font-sans">
	<Navbar />
	<main>
		<slot />
	</main>
</div>