<script lang="ts">
	import Navbar from '$lib/components/Navbar.svelte';
</script>

<div class="min-h-screen bg-slate-50 font-sans">
	<Navbar />
	<main>
		<slot />
	</main>
</div>