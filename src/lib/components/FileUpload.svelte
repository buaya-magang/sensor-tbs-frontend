<script lang="ts">
	// Variabel untuk menyimpan status
	import ProgressBar from '$lib/components/ProgressBar.svelte';
	let predictionResult: { prediction: string; confidence: string } | null = null;
	let isLoading = false;
	let errorMessage = '';
	let previewUrl: string | null = null; // Variabel untuk URL preview gambar

	// Ganti dengan URL API Anda yang ada di Hugging Face Spaces
	const API_URL = 'https://aryairfan-tbs-api.hf.space/predict';

	// Fungsi ini akan berjalan ketika pengguna memilih file
	async function handleFileSelect(event: Event) {
		const target = event.target as HTMLInputElement;
		const file = target.files?.[0];

		if (!file) return;

		// Reset status sebelum request baru
		isLoading = true;
		errorMessage = '';
		predictionResult = null;
		
		// Buat URL sementara untuk preview gambar
		if (previewUrl) {
			URL.revokeObjectURL(previewUrl); // Hapus URL lama untuk mencegah memory leak
		}
		previewUrl = URL.createObjectURL(file);

		const formData = new FormData();
		formData.append('file', file);

		try {
			// Kirim request ke API menggunakan fetch
			const response = await fetch(API_URL, {
				method: 'POST',
				body: formData
			});

			const data = await response.json();

			if (!response.ok) {
				// Ambil pesan error dari API jika ada, jika tidak gunakan statusText
				throw new Error(data.error || `Error: ${response.statusText}`);
			}
			
			predictionResult = data;

		} catch (error: any) {
			console.error('Gagal menghubungi API:', error);
			errorMessage = error.message || 'Gagal menghubungi server. Silakan coba lagi.';
		} finally {
			// Pastikan loading berhenti setelah selesai
			isLoading = false;
		}
	}
</script>

<div class="space-y-8">
	<label
	for="file-upload"
	class="block border-2 border-dashed border-blue-400 rounded-lg p-4 text-center cursor-pointer hover:bg-blue-50/50 transition-colors min-h-[150px] flex justify-center items-center"
>
	{#if !previewUrl}
		<p class="text-gray-500">
			Drag image file here or <span class="text-blue-600 font-semibold">click to browse</span>
		</p>
	{:else}
		<img src={previewUrl} alt="Preview Gambar" class="max-h-48 object-contain rounded-md" />
	{/if}
	</label>
	<input
		type="file"
		id="file-upload"
		class="hidden"
		accept="image/png, image/jpeg"
		on:change={handleFileSelect}
	/>

	{#if isLoading}
		<div class="space-y-3 text-center p-4">
			<p class="text-blue-600 font-semibold animate-pulse">Menganalisis Gambar...</p>
			<ProgressBar />
		</div>
		{:else if predictionResult}
			<div class="text-left bg-white p-6 rounded-lg shadow-md border border-gray-200">
				<h3 class="font-bold text-lg mb-3">Hasil Prediksi:</h3>
				<p class="text-base mb-1">
					<strong>Status:</strong>
					<span class="font-mono text-lg ml-2 px-3 py-1 rounded-full bg-green-100 text-green-800">
						{predictionResult.prediction}
					</span>
				</p>
				<p class="text-base">
					<strong>Tingkat Keyakinan:</strong>
					<span class="font-mono text-lg ml-2">
						{parseFloat(predictionResult.confidence).toFixed(2) * 100}%
					</span>
				</p>
			</div>
		{:else if errorMessage}
		<div class="text-center p-4 bg-red-100 text-red-700 rounded-lg">
			<p>{errorMessage}</p>
		</div>
	{/if}
</div>