<template>
  <div class="min-h-screen bg-gradient-to-tr from-neutral-950 via-[#29134C] to-neutral-950 text-white font-['Kanit',sans-serif] flex flex-col justify-between">
    
    <Navbar />

    <!-- Main Content -->
    <div class="flex-grow">
      <main class="flex flex-col items-center px-4 py-12">
        
         <!-- Page title -->
        <div class="relative inline-block mb-6 mt-5">
          <h1 class="text-4xl text-white mb-12 mt-5 tracking-wider">
            Certification
          </h1>
          <span class="absolute top-17 left-1/2 -translate-x-1/2 w-19 h-1 bg-[#9a2fdc] rounded-full"></span>
        </div>
        
        <!-- Icon -->
        <div class="-mt-8 p-3 rounded-2xl bg-purple-900/15 hover:bg-purple-900/40 duration-500 border border-purple-500/30 shadow-lg shadow-purple-950/50 flex items-center justify-center">
          <HugeiconsIcon :icon="Certificate01Icon" :size="40" class="text-[#9a2fdc]"/>
        </div>
      </main>

      <!-- Card Container -->
      <section>
        <CertCard 
          :certificates="certificates"
          @open="(imgSrc) => selectedImage = imgSrc"/>
      </section>
    </div>

    <!-- Picture enlargement function-->
    <dialog class="modal" :class="{'modal-open': selectedImage}">
      <div class="modal-box bg-neutral-900/95 border border-violet-500/40 p-6 max-w-3xl relative flex items-center justify-center">
        <img class="w-full h-auto rounded-lg max-h-[75vh] object-contain mx-auto shadow-2xl"
          v-if="selectedImage" 
          :src="selectedImage" 
          alt="Certificate Preview"/>
      </div>
      
			<form method="dialog" class="modal-backdrop bg-purple/80">
        <button @click="selectedImage = null" type="button">close</button>
      </form>
    </dialog>

  </div>
</template>

<script setup>
  import {HugeiconsIcon} from '@hugeicons/vue';
  import {Certificate01Icon} from '@hugeicons/core-free-icons'
  import {ref} from 'vue'
  const selectedImage = ref(null)

	//Certs in array
	const certificates = [
    {
			title: 'IT Specialist - Databases', 
			img: '/images/it-specialist-database.jpg',
			verifyUrl: 'https://www.certiport.com/portal/pages/credentialverification.aspx'
		},
		{
			title: 'MS Word Associate', 
			img: '/images/ms-word-associate.jpg',
			verifyUrl: 'https://www.certiport.com/portal/pages/credentialverification.aspx'
		},
		{
			title: 'MS Excel Associate',
			img: '/images/ms-excel-associate.jpg',
			verifyUrl: 'https://www.certiport.com/portal/pages/credentialverification.aspx'
		}
	]

	useHead({
		title: 'Certification | Jasmin Sabater'
	})

	useSeoMeta({
		title: 'Certification | Jasmin Sabater',
		ogTitle: 'Certification | Jasmin Sabater',
		description: 'View certifications and credentials earned by Jasmin Sabater.',
		ogDescription: 'View certifications and credentials earned by Jasmin Sabater.',
		ogImage: '/images/profile.JPG',
		twitterCard: 'summary_large_image',
	})
</script>