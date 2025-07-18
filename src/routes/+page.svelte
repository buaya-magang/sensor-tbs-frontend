<script lang="ts">
	import tbsImage from '$lib/assets/tbs-illustration.png'; // Ganti dengan path gambar Anda
</script>

<div class="container mx-auto grid grid-cols-1 md:grid-cols-2 items-center gap-12 px-4 py-16 text-center md:text-left">
	<div class="space-y-6">
		<h1 class="text-4xl md:text-5xl font-bold text-gray-800 leading-tight">
			Klasifikasi Kematangan TBS Kelapa Sawit
		</h1>
		<p class="text-gray-600">
			Sistem ini memanfaatkan model deep learning ResNet50 untuk menentukan kematangan TBS berdasarkan input gambar.
		</p>
		<a href="/klasifikasi" class="inline-block bg-blue-600 text-white font-bold py-3 px-8 rounded-lg hover:bg-blue-700 transition-transform hover:scale-105">
			Mulai Klasifikasi →
		</a>
	</div>
	<div>
		<img src={tbsImage} alt="Ilustrasi Tandan Buah Segar" class="w-full max-w-md mx-auto" />
	</div>
</div>