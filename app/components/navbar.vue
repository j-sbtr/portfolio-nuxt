<template>
  <header class="sticky top-4 z-50 w-full flex justify-center">
    <nav class="navbar bg-glass min-h-[60px] h-[60px] px-10 font-['Kanit',sans-serif] text-white border border-purple-900/30 rounded-full shadow-xl shadow-violet-900/20 backdrop-blur-3xl
        w-md sm:w-xl md:w-2xl lg:w-3xl xl:w-4xl 2xl:w-5xl">
      <!-- Logo -->
      <div class="navbar-start">
        <NuxtLink to="/" class="text-[22px] font-bold text-white hover:text-[#9a2fdc] transition-colors duration-500">
          JSS
        </NuxtLink>
      </div>

      <!-- Desktop Menu-->
      <div class="navbar-end hidden md:flex">
        <ul class="flex items-center gap-11 list-none m-0 p-0">
          <li>
            <NuxtLink to="/" class="relative group text-[18px] text-white no-underline whitespace-nowrap [&.router-link-active]:text-[#9a2fdc]">
              <span class="absolute bottom-0 left-0 w-0 h-[2px] bg-[#9a2fdc] transition-all duration-300 group-hover:w-full"></span>
              Home
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to="/about" class="relative group text-[18px] text-white no-underline whitespace-nowrap [&.router-link-active]:text-[#9a2fdc]">
              <span class="absolute bottom-0 left-0 w-0 h-[2px] bg-[#9a2fdc] transition-all duration-300 group-hover:w-full"></span>
              About
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to="/tech-stack" class="relative group text-[18px] text-white no-underline whitespace-nowrap [&.router-link-active]:text-[#9a2fdc]">
              <span class="absolute bottom-0 left-0 w-0 h-[2px] bg-[#9a2fdc] transition-all duration-300 group-hover:w-full"></span>
              Tech Stack
            </NuxtLink>
          </li>
          <li>
            <NuxtLink to="/certificate" class="relative group text-[18px] text-white no-underline whitespace-nowrap [&.router-link-active]:text-[#9a2fdc]">
              <span class="absolute bottom-0 left-0 w-0 h-[2px] bg-[#9a2fdc] transition-all duration-300 group-hover:w-full"></span>
              Certification
            </NuxtLink>
          </li>
        </ul>
      </div>

      <!-- Mobile Menu / Hamburger -->
      <div class="navbar-end md:hidden">
        <div class="dropdown dropdown-end">
          <div tabindex="0" role="button" class="btn btn-ghost btn-circle text-white text-[30px] pt-1">
            <HugeiconsIcon :icon="Menu01Icon" size="23"/>
          </div>
          
          <!-- Dropdown Menu #341b5f-->
          <ul tabindex="0" class="dropdown-content menu menu-sm mt-3 z-[1] p-2 bg-neutral-900 rounded-box w-60 text-center text-white border border-purple-900/40">
            <li class="py-1">
              <NuxtLink to="/" class="text-[18px] text-white hover:text-[#9a2fdc] active:bg-purple-900/50 active:text-white
              transition-colors duration-500 justify-center whitespace-nowrap [&.router-link-active]:bg-purple-800/50">
                Home
              </NuxtLink>
            </li>

            <li class="py-1">
              <NuxtLink to="/about" class="text-[18px] text-white hover:text-[#9a2fdc] active:bg-purple-900/50 active:text-white
              transition-colors duration-500 justify-center whitespace-nowrap [&.router-link-active]:bg-purple-900/50">
                About
              </NuxtLink> 
            </li>

            <li class="py-1">
              <NuxtLink 
              to="/tech-stack" class="text-[18px] text-white hover:text-[#9a2fdc] active:bg-purple-900/50 active:text-white
              transition-colors duration-500 justify-center whitespace-nowrap [&.router-link-active]:bg-purple-900/50">
                Tech Stack
              </NuxtLink>
            </li>
            
            <li class="py-1">
              <NuxtLink to="/certificate" class="text-[18px] text-white hover:text-[#9a2fdc] active:bg-purple-900/50 active:text-white
              transition-colors duration-500 justify-center whitespace-nowrap [&.router-link-active]:bg-purple-900/50">
                Certification
              </NuxtLink>
            </li>
          </ul>
        </div>
      </div>

    </nav>
  </header>
</template>

<script setup>
  import {HugeiconsIcon} from '@hugeicons/vue';
  import {Menu01Icon} from '@hugeicons/core-free-icons'
</script>