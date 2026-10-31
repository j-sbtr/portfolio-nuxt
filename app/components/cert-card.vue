<template>
  <div class="card-container flex justify-center flex-wrap">
    <div 
      v-for="cert in certificates" 
      :key="cert.title"
      class="card max-w-sm rounded-lg m-10 mt-1 px-4 py-2 group hover:shadow-2xl hover:bg-purple-900/20
			hover:border-white md:min-w-md lg:min-w-lg bg-gray-800/25 border border-gray-700 flex flex-col justify-between">
      
			<div>
        <img 
          :src="cert.img" 
          :alt="cert.title"
          class="cert-img w-full h-auto border border-gray-700 rounded-md group-hover:border-white cursor-pointer"
          @click="$emit('open', cert.img)">

				<!-- Cert name -->
        <div class="card-content">
          <h2 class="text-3xl mt-3 ml-2 mr-2 mb-1 text-center">{{ cert.title }}</h2>
        </div>
      </div>

			<!-- Validation btn -->
      <div class="flex justify-end mt-4">
        <a 
          :href="cert.verifyUrl" 
          target="_blank" 
          rel="noopener noreferrer"
          class="btn m-2 -mt-1 border bg-gray-800/25 border-gray-700 hover:border-white hover:scale-105 duration-500 hover:bg-purple-900/40 tracking-widest text-white">
          Validate Here
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