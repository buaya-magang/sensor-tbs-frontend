<script lang="ts">
	// Path gambar diperbaiki sesuai file yang sudah Anda upload
	import tbsImage from '$lib/assets/tbs-illustration.png';
</script>

<div class="container mx-auto grid grid-cols-1 items-center gap-y-10 px-10 pt-14 lg:grid-cols-2 lg:gap-x-12">
	
	<div class="order-2 flex flex-col justify-center space-y-6 text-center lg:order-1 lg:text-left">
		<h1 class="text-4xl font-bold text-gray-800 lg:text-5xl">
			SensorTBS
		</h1>
		<p class="text-gray-600">
			Aplikasi ini bertujuan untuk meningkatkan efisiensi dan akurasi dalam klasifikasi TBS, yang pada gilirannya akan membantu pengelolaan dan pengambilan keputusan yang lebih baik dalam pertanian kelapa sawit.
		</p>
		<p class="text-gray-600">
			Pengguna dapat mengunggah gambar TBS. Prediksi dilakukan menggunakan model pembelajaran mesin yang telah dilatih berdasarkan data gambar yang diambil langsung dari lapangan.
		</p>
		<div class="flex flex-col items-center sm:flex-row sm:justify-center lg:justify-start">
			<a
				href="/klasifikasi"
				class="inline-block rounded-lg bg-blue-600 px-8 py-3 font-bold text-white transition-transform hover:scale-105 hover:bg-blue-700"
			>
				Mulai Klasifikasi →
			</a>
		</div>
	</div>

	<div class="order-1 lg:order-2">
		<img
			src={tbsImage}
			class="mx-auto h-auto w-full max-w-md animate-float"
			alt="Ilustrasi Tandan Buah Segar"
		/>
	</div>
	
</div>