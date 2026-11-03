<template>
  <div class="min-h-screen bg-gradient-to-tr from-neutral-950 via-[#29134C] to-neutral-950 text-white flex flex-col">
    
    <!-- Default ng nuxt -->
    <Navbar />

    <!-- Content -->
    <main class="flex-grow flex items-center justify-center px-6 py-12 md:-mt-50 lg:-mt-50 font-['Kanit',sans-serif]">
      <section class="flex flex-col items-center max-w-7xl mx-auto md:flex-row md:justify-between md:items-center w-full gap-12">

        <!-- Picture -->
        <div class="flex justify-center md:w-1/2">
          <div class="avatar">
            <div class="w-48 h-48 md:w-72 md:h-72 rounded-full ring ring-violet-800 ring-offset-base-100 ring-offset-2 shadow-2xl">
              <img src="/images/profile.JPG" alt="Jasmin Sabater Profile" class="object-cover"/>
            </div>
          </div>
        </div>

        <!-- Text Content -->
        <div class="text-center md:text-left md:w-1/2 space-y-4">
          <div>
            <h1 class="text-4xl font-semibold tracking-wide text-neutral-300">Hi! I am</h1>
            <h2 class="text-5xl md:text-6xl font-extrabold text-violet-400 drop-shadow-[0_2px_8px_rgba(139,92,246,0.3)] mt-1">Jasmin Sabater</h2>
          </div>
          
          <p class="text-neutral-300 text-lg leading-relaxed max-w-xl">
            A student eager to learn, grow, and explore technology to make a positive impact and contribute to the future.
          </p>
          
          <div class="pt-2">
            <p class="text-[20px] font-semibold tracking-wider text-neutral-400 uppercase mb-1">Connect with me</p>
            
            <!-- Icons -->
            <!-- GitHub -->
            <div class="inline-flex gap-3 ml-3">
              <a href="https://github.com/j-sbtr" target="_blank" 
                class="group btn btn-circle btn-lg btn-neutral bg-neutral-900 border-violet-800/50 hover:bg-neutral-900/20 text-white">
                <HugeiconsIcon :icon="GithubIcon" size="23" color="currentColor"
                  class="text-neutral-300 group-hover:text-violet-800 transition-colors duration-300"/>
              </a>
            </div>
            
            <!-- LinkedIn -->
            <div class="inline-flex gap-3 ml-3">
              <a href="https://www.linkedin.com/in/j-sabater/" target="_blank" 
                class="group btn btn-circle btn-lg btn-neutral bg-neutral-900 border-violet-800/50 hover:bg-neutral-900/20 text-white">
                <HugeiconsIcon :icon="Linkedin02Icon" size="23" color="currentColor"
                  class="text-neutral-300 group-hover:text-violet-800 transition-colors duration-300"/>
              </a>
            </div>
          </div>
        </div>

      </section>
    </main>

  </div>
</template>

<script setup>
  import {HugeiconsIcon} from '@hugeicons/vue';
  import {GithubIcon, Linkedin02Icon} from '@hugeicons/core-free-icons'

  useHead({
    title: 'Home | Jasmin Sabater'
  })

  useSeoMeta({
    ogTitle: 'Jasmin Sabater | Portfolio',
    description: 'An aspiring IT professional exploring tech to build impactful web solutions.',
    ogDescription: 'An aspiring IT professional exploring tech to build impactful web solutions.',
    ogImage: '/images/profile.JPG',
    twitterCard: 'summary_large_image',
  })
</script>