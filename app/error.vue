<script setup lang="ts">

useHead({
  title: 'Page Not Found'
})

</script>

<template>
  <div class="min-h-screen bg-gradient-to-tr from-neutral-950 via-[#29134C] to-neutral-950 text-white flex flex-col items-center justify-center px-6 font-['Kanit',sans-serif]">
    <div class="text-center max-w-md mx-auto space-y-6">
      
      <!-- 404 Error -->
      <h1 class="text-8xl font-black text-violet-400 tracking-wider">
        404
      </h1>

      <!-- Error Content -->
      <div class="space-y-2">
        <h2 class="text-3xl font-semibold text-neutral-200">
          Page Not Found
        </h2>
        <p class="text-neutral-300 text-lg leading-relaxed">
          The page you are looking for doesn't exist or has been moved.
        </p>
      </div>

      <!-- Back to Home Button -->
      <div class="pt-4">
        <NuxtLink 
          to="/" 
          class="btn bg-purple-900/50 hover:bg-purple-800 text-white border-violet-700/50 hover:border-violet-600 px-8 rounded-full shadow-lg transition-all duration-300"
        >
          Go Back Home
        </NuxtLink>
      </div>

    </div>
  </div>
</template>