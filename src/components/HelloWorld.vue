<template>
  <div class="min-h-screen bg-neutral-950 text-neutral-100 overflow-x-hidden">
    <!-- Header -->
    <header class="w-full flex items-center justify-between px-6 py-4 border-b border-neutral-800">
      <h1 class="text-2xl font-bold tracking-tight">EcoCore</h1>

      <nav class="hidden md:flex gap-6 text-sm">
        <a href="#features" class="hover:text-green-400 transition">Características</a>
        <a href="#screens" class="hover:text-green-400 transition">Interfaz</a>
        <a href="#download" class="hover:text-green-400 transition">Descargar</a>
      </nav>

      <button class="md:hidden" @click="mobileOpen = !mobileOpen">
        <span class="i-lucide-menu text-2xl"></span>
      </button>
    </header>

    <!-- Mobile Menu -->
    <transition name="fade">
      <div
        v-if="mobileOpen"
        class="md:hidden flex flex-col gap-4 bg-neutral-900 p-6 border-b border-neutral-800"
      >
        <a href="#features" class="hover:text-green-400 transition">Características</a>
        <a href="#screens" class="hover:text-green-400 transition">Interfaz</a>
        <a href="#download" class="hover:text-green-400 transition">Descargar</a>
      </div>
    </transition>

    <!-- Hero -->
    <section class="px-6 py-20 flex flex-col md:flex-row items-center justify-between gap-14">
      <div class="max-w-xl space-y-6">
        <h2 class="text-5xl font-bold leading-tight">
          Tu app para impulsar el <span class="text-green-400">reciclaje inteligente</span>
        </h2>
        <p class="text-neutral-400 text-lg">
          EcoCore te ayuda a encontrar centros de reciclaje, gestionar tus materiales,
          y participar en una comunidad más sustentable.
        </p>

        <a
          href="#download"
          class="inline-block bg-green-500 text-black font-semibold px-6 py-3 rounded-xl hover:bg-green-400 transition text-lg"
        >
          Descargar APK
        </a>
      </div>

      <div class="w-full md:w-auto">
        <div class="rounded-3xl border border-neutral-800 bg-neutral-900 p-4 shadow-xl">
          <img
            src="/mockup-phone.png"
            alt="App Mockup"
            class="w-72 md:w-96 drop-shadow-2xl"
          />
        </div>
      </div>
    </section>

    <!-- Features -->
    <section id="features" class="px-6 py-24 border-t border-neutral-800">
      <h3 class="text-center text-4xl font-bold mb-16">Características principales</h3>

      <div class="grid md:grid-cols-3 gap-12 max-w-5xl mx-auto">
        <div class="p-6 bg-neutral-900 border border-neutral-800 rounded-2xl">
          <h4 class="text-xl font-semibold mb-2">Centros cercanos</h4>
          <p class="text-neutral-400">Encuentra recicladoras cerca de ti con datos actualizados.</p>
        </div>

        <div class="p-6 bg-neutral-900 border border-neutral-800 rounded-2xl">
          <h4 class="text-xl font-semibold mb-2">Registro de materiales</h4>
          <p class="text-neutral-400">Lleva control de lo que reciclas fácilmente.</p>
        </div>

        <div class="p-6 bg-neutral-900 border border-neutral-800 rounded-2xl">
          <h4 class="text-xl font-semibold mb-2">Comunidad sustentable</h4>
          <p class="text-neutral-400">Conecta con otros usuarios y comparte tus logros.</p>
        </div>
      </div>
    </section>

    <!-- Download -->
    <section id="download" class="px-6 py-24 border-t border-neutral-800 text-center">
      <h3 class="text-4xl font-bold mb-6">Descargar la aplicación</h3>
      <p class="text-neutral-400 mb-10 max-w-xl mx-auto">
        Disponible en formato APK para Android. Muy pronto en App Store y Play Store.
      </p>

      <a
        href="/app-release.apk"
        class="inline-block bg-green-500 text-black font-semibold px-8 py-4 rounded-xl hover:bg-green-400 transition text-lg"
      >
        Descargar APK
      </a>
    </section>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const mobileOpen = ref(false)
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: opacity .25s ease;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>