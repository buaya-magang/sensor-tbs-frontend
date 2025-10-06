<script lang="ts">
	import tbsImage from '$lib/assets/tbs-illustration.png';
	import { viewport } from '$lib/actions/viewport.js';
</script>

<!-- Hero Section -->
<div
	class="container mx-auto max-w-6xl grid grid-cols-1 md:grid-cols-2 items-center gap-10 px-6 lg:px-12 py-20 md:py-28"
>
	<!-- Kolom Teks -->
	<div class="order-2 md:order-1 flex flex-col justify-center space-y-6 text-center md:text-left">
		<h1
			use:viewport
			class="fade-up text-3xl sm:text-4xl md:text-5xl font-bold text-gray-800 leading-tight"
		>
			SensorTBS: <br class="hidden sm:block" /> Klasifikasi Kematangan TBS
		</h1>

		<p
			use:viewport
			class="fade-up text-gray-600 text-base sm:text-lg max-w-lg mx-auto md:mx-0"
			style="transition-delay: 150ms;"
		>
			Sistem ini memanfaatkan model deep learning <strong>ResNet50</strong> untuk menentukan tingkat kematangan
			buah kelapa sawit berdasarkan input gambar.
		</p>

		<div
			use:viewport
			class="fade-up flex flex-col items-center sm:flex-row sm:justify-center md:justify-start"
			style="transition-delay: 300ms;"
		>
			<a
				href="/klasifikasi"
				class="inline-block rounded-lg bg-blue-600 px-8 py-3 font-bold text-white transition-transform hover:scale-105 hover:bg-blue-700 shadow-md"
			>
				Mulai Klasifikasi →
			</a>
		</div>
	</div>

	<!-- Kolom Gambar -->
	<div use:viewport class="zoom-in order-1 md:order-2 flex justify-center md:justify-end">
		<img
			src={tbsImage}
			alt="Ilustrasi Kelapa Sawit"
			class="w-64 sm:w-80 md:w-[420px] lg:w-[460px] h-auto drop-shadow-md animate-float"
		/>
	</div>
</div>
