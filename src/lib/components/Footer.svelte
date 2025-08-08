<script lang="ts">
	const currentYear = new Date().getFullYear();
</script>

<footer class="mt-20 border-t border-slate-200">
	<div class="container mx-auto px-4 py-8">
		<div class="flex flex-col items-center gap-4 sm:flex-row sm:justify-between">
			
			<div class="text-center text-sm text-slate-500 sm:text-left">
				<p>&copy; {currentYear} SensorTBS. byKasolll</p>
			</div>

			<div class="text-sm font-medium text-slate-500">
				<ul class="flex items-center space-x-6">
					<li><a href="/" class="transition-colors hover:text-slate-900">Home</a></li>
					<li><a href="/klasifikasi" class="transition-colors hover:text-slate-900">Classification</a></li>
					<li><a href="/about" class="transition-colors hover:text-slate-900">About</a></li>
				</ul>
			</div>

		</div>
	</div>
</footer>