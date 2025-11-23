<template>
  <div class="min-h-screen bg-neutral-950 text-neutral-100 flex flex-col overflow-x-hidden">

    <!-- HEADER -->
    <header class="w-full fixed top-0 left-0 z-50 backdrop-blur-xl bg-neutral-900/60 border-b border-neutral-800">
      <div class="max-w-6xl mx-auto flex items-center justify-between px-6 py-4">
        <h1 class="text-xl font-bold tracking-tight">Eco Core</h1>

        <nav class="hidden md:flex gap-6 text-neutral-300 text-sm">
          <a href="#preview" class="hover:text-green-400 transition">Vista previa</a>
          <a href="#features" class="hover:text-green-400 transition">Características</a>
          <a href="#download" class="hover:text-green-400 transition">Descargar</a>
        </nav>

        <a
          href="#download"
          class="px-4 py-2 rounded-xl text-sm font-semibold bg-green-500 hover:bg-green-600 transition shadow-lg hover:shadow-green-500/20"
        >
          Descargar
        </a>
      </div>
    </header>


    <!-- HERO SIN IMÁGENES → SOLO FORMAS, GLOW Y ANIMACIONES -->
    <section class="relative pt-32 pb-24 flex flex-col items-center text-center px-6 overflow-hidden">

      <!-- Glow dinámico -->
      <div class="absolute -top-40 w-[600px] h-[600px] bg-green-500/20 blur-[160px] rounded-full animate-pulse-slow"></div>

      <h1 class="text-5xl md:text-7xl font-extrabold tracking-tight animate-fade-in-up">
        Eco Core
      </h1>

      <p class="text-neutral-300 text-lg md:text-xl max-w-xl mt-4 animate-fade-in-up delay-200">
        Una experiencia sustentable. Moderna. Rápida. Diseñada para impactar.
      </p>

      <div class="mt-8 flex gap-4 animate-fade-in-up delay-300">
        <a
          href="#download"
          class="px-8 py-4 rounded-2xl text-lg font-semibold bg-green-500 hover:bg-green-600 transition-all shadow-xl hover:shadow-green-500/30"
        >
          Descargar APK
        </a>
        <a
          href="#features"
          class="px-8 py-4 rounded-2xl text-lg font-semibold bg-neutral-900 border border-neutral-800 hover:bg-neutral-800 transition-all"
        >
          Ver Más
        </a>
      </div>

      <!-- Figura decorativa 3D-like -->
<div class=" p-4  rounded-3xl  shadow-green-500/10 rotate-3 hover:rotate-0 transition duration-700 animate-float">
  <img 
    src="/mockup.png"
    alt="Mockup de la app"
    class="w-full h-auto rounded-2xl"
  />
</div>
    </section>


    <!-- FEATURES SIN IMÁGENES -->
    <section id="features" class="px-6 py-24 flex flex-col items-center">
      <h2 class="text-3xl font-semibold mb-14">¿Por qué Eco Core?</h2>

      <div class="grid grid-cols-1 md:grid-cols-3 gap-8 max-w-5xl">

      

        <div class="p-8 bg-neutral-900 rounded-2xl border border-neutral-800 hover:border-green-500 hover:shadow-lg hover:shadow-green-500/20 transition-all">
          <h3 class="text-xl font-bold mb-2">Gestión inteligente</h3>
          <p class="text-neutral-400">Del escombro al Activo Digital.</p>
        </div>

       

      </div>
    </section>


    <!-- DOWNLOAD SECTION -->
    <section id="download" class="text-center py-24 px-6">
      <h2 class="text-3xl font-semibold mb-6">Descargar Eco Core</h2>
      <p class="text-neutral-400 max-w-md mx-auto mb-10">Descarga la versión más reciente en un clic.</p>

     <a
href="https://drive.google.com/file/d/1Bm02B1J50hghqufy3C3sBeMZxRyFdt88/view?usp=sharing"
class="px-10 py-4 rounded-2xl text-lg font-semibold bg-green-500 hover:bg-green-600 transition-all shadow-xl hover:shadow-green-500/30"
> Descargar APK</a>
    </section>


    <!-- FOOTER -->
    <footer class="py-10 text-center text-neutral-500 text-sm">
      © 2025 Eco Core — Innovando por un futuro sostenible.
    </footer>

  </div>
</template>

<script setup>
// No JS por ahora
</script>

<style>
@keyframes fade-in-up {
  0% { opacity: 0; transform: translateY(20px); }
  100% { opacity: 1; transform: translateY(0); }
}

.animate-fade-in-up {
  animation: fade-in-up 0.8s ease forwards;
}

@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-12px); }
}

.animate-float {
  animation: float 4s ease-in-out infinite;
}

@keyframes pulse-slow {
  0%, 100% { opacity: 0.3; }
  50% { opacity: 0.6; }
}

.animate-pulse-slow {
  animation: pulse-slow 6s ease-in-out infinite;
}
</style>