<template>
  <!-- Main Container -->
  <div class="card-container flex justify-center flex-wrap">
    <div class="card max-w-sm rounded-lg m-10 mt-1 px-4 py-2 group hover:shadow-2xl hover:bg-purple-900/2 
  hover:border-purple-400/50 hover:scale-105 transition-transform duration-300 md:min-w-md lg:min-w-lg bg-gray-800/25 border border-gray-700 flex flex-col justify-between"
      v-for="cert in certificates" 
      :key="cert.title">
      
      <!-- Cert img -->
			<div>
        <img 
          :src="cert.img" 
          :alt="cert.title"
          class="cert-img w-full h-auto border border-gray-700 rounded-md group-hover:border-violet cursor-pointer"
          @click="$emit('open', cert.img)">

				<!-- Cert name -->
        <div class="card-content">
          <h2 class="text-3xl mt-3 ml-2 mr-2 mb-1 text-center">{{cert.title}}</h2>
        </div>
      </div>

			<!-- Validation btn -->
      <div class="flex justify-end mt-4">
        <a class="btn m-2 -mt-1 border bg-gray-800/25 border-gray-700 hover:border-white hover:scale-105 duration-500 hover:bg-purple-900/40 tracking-widest text-white"
          :href="cert.verifyUrl" 
          target="_blank" 
          rel="noopener noreferrer">
          <span>Validate Here</span>
        </a>
      </div>

    </div>
  </div>
</template>

<script setup>
	defineProps({
		certificates: {
			type: Array,
			required: true
		}
	})

	defineEmits(['open'])
</script>