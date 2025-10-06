<script lang="ts">
    import tbsImage from '$lib/assets/tbs-illustration.png';
    import { viewport } from '$lib/actions/viewport.js';
</script>

<div class="container mx-auto grid max-w-6xl grid-cols-1 items-center gap-y-10 px-10 pt-14 md:grid-cols-2 md:gap-x-12">
    
            <div class="order-2 flex flex-col justify-center space-y-6 text-center md:order-1 md:text-left">
        <h1 use:viewport class="fade-up text-4xl font-bold text-gray-800 md:text-5xl">
            Klasifikasi Kematangan TBS
        </h1>
        <p use:viewport class="fade-up text-gray-600" style="transition-delay: 150ms;">
            Sistem ini memanfaatkan model deep learning ResNet50 untuk menentukan Tingkat Kematangan Buah Kelapa Sawit berdasarkan
            input gambar.
        </p>
        
                <div use:viewport class="fade-up flex flex-col items-center sm:flex-row sm:justify-center md:justify-start" style="transition-delay: 300ms;">
            <a
                href="/klasifikasi"
                class="inline-block rounded-lg bg-blue-600 px-8 py-3 font-bold text-white transition-transform hover:scale-105 hover:bg-blue-700"
            >
                Mulai Klasifikasi →
            </a>
        </div>
    </div>

        <div use:viewport class="zoom-in order-1 md:order-2">
        <img
            src={tbsImage}
            class="mx-auto h-auto w-full max-w-md animate-float"
            alt="Ilustrasi Kelapa Sawit"
        />
    </div>
    
</div>