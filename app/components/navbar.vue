<template>
  <div class="navbar bg-[#341b5f] min-h-[60px] h-[60px] px-10 font-['Kanit',sans-serif] sticky top-0 z-50 text-white border-b border-purple-900/30">
    
    <!-- Logo -->
    <div class="navbar-start">
      <NuxtLink to="/" class="text-[22px] font-bold pl-3 text-white hover:opacity-90 transition-opacity">
        JSS
      </NuxtLink>
    </div>

    <!-- Desktop Menu-->
    <div class="navbar-end hidden md:flex">
      <ul class="flex items-center gap-11 list-none m-0 p-0">
        <li>
          <NuxtLink to="/" class="text-[18px] text-white no-underline transition-colors duration-500 hover:text-[#9a2fdc] whitespace-nowrap">
            Home
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/about" class="text-[18px] text-white no-underline transition-colors duration-500 hover:text-[#9a2fdc] whitespace-nowrap">
            About
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/tech-stack" class="text-[18px] text-white no-underline transition-colors duration-500 hover:text-[#9a2fdc] whitespace-nowrap">
            Tech Stack
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/certificate" class="text-[18px] text-white no-underline transition-colors duration-500 hover:text-[#9a2fdc] whitespace-nowrap">
            Certification
          </NuxtLink>
        </li>
      </ul>
    </div>

    <!-- Mobile Menu / Hamburger -->
    <div class="navbar-end md:hidden">
      <div class="dropdown dropdown-end">
        <div tabindex="0" role="button" class="btn btn-ghost btn-circle text-white text-[30px] pt-1">
          <ion-icon name="menu-outline"></ion-icon>
        </div>
        
        <!-- Dropdown Menu focus:bg-purple-900/50 focus:text-white active:bg-purple-900/50 active:text-white-->
        <ul tabindex="0" class="dropdown-content menu menu-sm mt-3 z-[1] p-2 shadow bg-[#341b5f] rounded-box w-52 text-center text-white border border-purple-900/40">
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

  </div>
</template>