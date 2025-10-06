<script lang="ts">
	// Tetap sama seperti sebelumnya
	import tbsImage from '$lib/assets/tbs-illustration.png';
	import { viewport } from '$lib/actions/viewport.js';
</script>

<!-- Wrapper utama -->
<div class="mx-auto max-w-screen-xl flex flex-col-reverse md:flex-row items-center justify-between gap-y-10 px-6 pt-20 md:pt-28 lg:px-16 min-h-[85vh]">

	<!-- Bagian teks -->
	<div class="flex flex-col justify-center space-y-6 text-center md:text-left w-full md:w-1/2 md:pl-4">
		<h1
			use:viewport
			class="fade-up text-3xl sm:text-4xl md:text-5xl font-bold text-gray-800 leading-tight"
		>
			Klasifikasi Kematangan TBS
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

	<!-- Bagian gambar -->
	<div use:viewport class="zoom-in flex justify-center md:justify-end w-full md:w-1/2">
		<img
			src={tbsImage}
			class="mx-auto h-auto w-64 sm:w-80 md:w-[420px] lg:w-[460px] animate-float drop-shadow-md"
			alt="Ilustrasi Kelapa Sawit"
		/>
	</div>
</div>
