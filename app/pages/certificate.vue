<template>
  <div class="min-h-screen bg-gradient-to-tr from-neutral-950 via-[#29134C] to-neutral-950 text-white font-['Kanit',sans-serif] flex flex-col justify-between">
    
    <Navbar />

    <!-- Main Content -->
    <div class="flex-grow">
      <main class="flex flex-col items-center px-4 py-12">
        <h1 class="text-4xl text-white mb-12 mt-5 tracking-wider">Certification</h1>
      </main>

      <!-- Card Container -->
      <section>
        <CertCard 
          :certificates="certificates"
          @open="(imgSrc) => selectedImage = imgSrc"/>
      </section>
    </div>

    <!-- Picture enlargement -->
    <dialog class="modal" :class="{ 'modal-open': selectedImage }">
      <div class="modal-box bg-neutral-900/95 border border-purple-500/40 p-6 max-w-3xl relative flex items-center justify-center">
        <img 
          v-if="selectedImage" 
          :src="selectedImage" 
          alt="Certificate Preview" 
          class="w-full h-auto rounded-lg max-h-[75vh] object-contain mx-auto shadow-2xl"/>
      </div>
      
			<form method="dialog" class="modal-backdrop bg-black/80">
        <button @click="selectedImage = null" type="button">close</button>
      </form>
    </dialog>

  </div>
</template>

<script setup>

	//Certs in array
	const certificates = [
    {
			title: 'IT Specialist in Database', 
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

	const selectedImage = ref(null)

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