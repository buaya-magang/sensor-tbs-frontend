<script lang="ts">
	// Pastikan path ke gambar Anda sudah benar.
	// Gambar ini bisa ditempatkan di folder `src/lib/assets/`.
	import tbsImage from '$lib/assets/tbs-illustration.png';
</script>

<div class="container mx-auto grid grid-cols-1 items-center gap-12 px-4 py-16 text-center md:grid-cols-2 md:text-left">
	
    <div class="space-y-6 md:order-first order-last">
		<h1 class="text-4xl font-bold leading-tight text-gray-800 md:text-5xl">
			Klasifikasi Kematangan TBS Kelapa Sawit
		</h1>
		<p class="text-gray-600">
			Sistem ini memanfaatkan model deep learning ResNet50 untuk menentukan kematangan TBS berdasarkan
			input gambar.
		</p>
		<a
			href="/klasifikasi"
			class="inline-block rounded-lg bg-blue-600 px-8 py-3 font-bold text-white transition-transform hover:scale-105 hover:bg-blue-700"
		>
			Mulai Klasifikasi →
		</a>
	</div>

	<div>
		<img
			src={tbsImage}
			alt="Ilustrasi Tandan Buah Segar"
			class="mx-auto w-full max-w-md animate-float"
		/>
	</div>
	
</div>