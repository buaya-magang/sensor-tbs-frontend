<script>import "../app.css";
import Navbar from '$lib/components/Navbar.svelte';</script>

<div class="min-h-screen bg-slate-50 font-sans">
	<Navbar></Navbar>
	<main>
		<slot></slot>
	</main>
</div>
