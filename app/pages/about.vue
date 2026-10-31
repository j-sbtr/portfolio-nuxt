<template>
  <div class="min-h-screen bg-gradient-to-tr from-neutral-950 via-[#29134C] to-neutral-950 text-white font-['Kanit',sans-serif] flex flex-col justify-between">
    
    <Navbar />

    <!-- Content -->
    <div class="flex-grow">
      <main class="flex flex-col items-center px-4 py-12">
        <h1 class="text-4xl text-white mb-12 mt-5 tracking-wider">About Me</h1>
      </main>

      <section>
        <div class="flex flex-col justify-center flex-wrap max-w-4xl mx-auto px-4 py-12 pt-0">
          
          <p class="mr-4 ml-4 mb-6 text-xl leading-relaxed text-neutral-300">
            I'm an undergraduate student pursuing a degree in Information Technology.
            I enjoy exploring how different systems work and how it connect people globally.
            My <span class="text-violet-400">curiosity</span> and 
            <span class="text-violet-400">desire to understand</span>
            the logic behind digital things motivate me to keep on learning and improving.
            My experience so far comes from the <span class="text-violet-400">academic projects</span> and 
            <span class="text-violet-400">hands-on activities</span>.
          </p>

          <p class="mr-4 ml-4 text-xl leading-relaxed text-neutral-300">
            I aspire to become a <span class="text-violet-400">skilled professional</span> in the IT field, 
            with <span class="text-violet-400">problem-solving</span>,
            <span class="text-violet-400">self-learning</span>, and 
            <span class="text-violet-400">collaboration</span>
            as my core strengths. Though I am still exploring my specialization, I have a growing interest in 
            <span class="text-violet-400">cybersecurity</span> and
            <span class="text-violet-400">database management</span>.
            My goal is to continuously grow into someone who can contribute meaningfully in the industry.
          </p>

        </div>
      </section>
    </div>

  </div>
</template>

<script setup>
useHead({
  title: 'About | Jasmin Sabater',
})

useSeoMeta({
  title: 'About | Jasmin Sabater',
  ogTitle: 'About | Jasmin Sabater',
  description: 'Learn more about Jasmin Sabater.',
  ogDescription: 'Learn more about Jasmin Sabater.',
  ogImage: '/images/profile.JPG',
  twitterCard: 'summary_large_image',
})
</script>