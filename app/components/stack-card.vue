<template>
	<!-- Outer card -->
  <div class="bg-gray-800/25 rounded-2xl p-7 h-full flex flex-col border border-gray-700 
	hover:border-purple-400/50 duration-300 hover:bg-purple-400/5">
    
		<div class="text-center mb-7">
      <h2 class="text-2xl font-bold text-purple-400 tracking-widest">{{ title }}</h2>
    </div>
    
    <!-- Item card -->
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 mb-0">
      <div 
        v-for="item in items" 
        :key="item.name"
        class="relative rounded-xl overflow-hidden bg-purple-400/10 border border-gray-400/50 
        hover:bg-purple-900/50 hover:scale-105 hover:border-white duration-300">

				<!-- Logo and divider -->
        <div class="h-32 flex items-center justify-center border-b border-gray-400/50">
          <img class="w-16 h-16 object-contain scale-110" 
          :src="item.img" 
          :alt="item.name">
        </div>
				
				<!-- Item name -->
        <div class="px-6 py-4 text-center flex-1 flex items-center justify-center">
          <div class="text-lg tracking-wider">{{ item.name }}</div>
        </div>

      </div>
    </div>

  </div>
</template>

<script setup>
	defineProps({
		title: {
			type: String,
			required: true},
		items: {
			type: Array,
			required: true}
	})
</script>