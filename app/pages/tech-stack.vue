<template>
  <div class="min-h-screen bg-gradient-to-tr from-neutral-950 via-[#29134C] to-neutral-950 text-white font-['Kanit',sans-serif] flex flex-col justify-between">
    
    <Navbar />

    <!-- Main Content -->
    <div class="flex-grow">
      <main class="flex flex-col items-center px-4 py-12">
        
         <!-- Page title -->
        <div class="relative inline-block mb-6 mt-5">
          <h1 class="text-4xl text-white mb-12 mt-5 tracking-wider">
            Tech Stack
          </h1>
          <span class="absolute top-17 left-1/2 -translate-x-1/2 w-19 h-1 bg-[#9a2fdc] rounded-full"></span>
        </div>
        
        <!-- Icon -->
        <div class="-mt-8 p-3 rounded-2xl bg-purple-900/15 hover:bg-purple-900/40 duration-500 border border-purple-500/30 shadow-lg shadow-purple-950/50 flex items-center justify-center">
          <HugeiconsIcon :icon="CodeIcon" :size="40" class="text-[#9a2fdc]"/>
        </div>
      </main>

      <!-- Card Container -->
      <section class="w-full">
        <div class="card-container grid grid-cols-1 p-20 pt-0 gap-10 p-10 items-stretch md:p-20 md:pt-0 lg:p-20 lg:pt-0 lg:max-w-7xl mx-auto">
          
          <!-- Languages & Frameworks Card -->
          <stack-card title="Languages & Frameworks" :items="languages" />

          <!-- Databases Card -->
          <stack-card title="Databases" :items="databases" />

          <!-- Tools Card -->
          <stack-card title="Tools" :items="tools" />

        </div>
      </section>
    </div>

  </div>
</template>

<script setup>
  import {HugeiconsIcon} from '@hugeicons/vue';
  import {CodeIcon} from '@hugeicons/core-free-icons'

  //Items per card in array
  const languages = [
		{name: 'Java', img: '/images/stacks/java.png'},
		{name: 'HTML', img: '/images/stacks/html.png'},
		{name: 'CSS', img: '/images/stacks/css.png'},
		{name: 'Tailwind CSS', img: '/images/stacks/tailwind-css.png'},
		{name: 'JavaScript', img: '/images/stacks/javascript.png'}
  ]

  const databases = [
		{name: 'PostgreSQL', img: '/images/stacks/postgresql.png'},
		{name: 'MongoDB', img: '/images/stacks/mongodb.png'}
   ]

  const tools = [
		{name: 'VS Code', img: '/images/stacks/visual-studio-code.png'},
		{name: 'SSMS', img: '/images/stacks/ssms.png'},
		{name: 'Android Studio', img: '/images/stacks/android-studio.png'},
		{name: 'Git', img: '/images/stacks/git.png'},
		{name: 'GitHub', img: '/images/stacks/github.png'}
  ]

  useHead({
		title: 'Tech Stack | Jasmin Sabater'
  })

  useSeoMeta({
    title: 'Tech Stack | Jasmin Sabater',
    ogTitle: 'Tech Stack | Jasmin Sabater',
    description: 'Explore the languages, databases, and development tools I use.',
    ogDescription: 'Explore the languages, databases, and development tools I use.',
    ogImage: '/images/profile.JPG',
    twitterCard: 'summary_large_image',
  })
</script>