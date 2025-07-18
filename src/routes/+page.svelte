<script lang="ts">
	// Ganti dengan path gambar Anda, misalnya di 'src/lib/assets/sawit.png'
	import tbsImage from '$lib/assets/sawit.png'; 
</script>

<div class="grid grid-cols-1 items-center gap-y-10 lg:grid-cols-2 lg:gap-x-12">
	
    <div class="order-2 flex flex-col justify-center space-y-6 lg:order-1">
		<h1 class="text-4xl font-bold text-gray-800">
			Klasifikasi Kematangan TBS Kelapa Sawit
		</h1>
		<p class="text-gray-600">
			Sistem ini memanfaatkan model deep learning ResNet50 untuk menentukan kematangan TBS berdasarkan
			input gambar.
		</p>
		<div class="flex flex-col sm:flex-row">
			<a
				href="/klasifikasi"
				class="inline-block rounded-lg bg-blue-600 px-8 py-3 font-bold text-white transition-transform hover:scale-105 hover:bg-blue-700"
			>
				Mulai Klasifikasi →
			</a>
		</div>
	</div>

	<div class="order-1 lg:order-2">
        <img src={tbsImage} class="h-auto w-full animate-float" alt="Ilustrasi Kelapa Sawit" />
	</div>

</div>