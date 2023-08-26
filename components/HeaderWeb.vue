<template>
      <header class="p-4 flex items-center justify-between font-bold border-2">
          <div class="flex items-center">
              <h1 class="text-3xl font-semibold">Hi.</h1>
          </div>
          <nav class="hidden md:flex space-x-4">
            <NuxtLink to="/" class="hover:underline">
              Me
            </NuxtLink>
            <NuxtLink to="/detail" class="hover:underline">
              Detail
            </NuxtLink>
            <NuxtLink to="/profil" class=" hover:underline">
              Profil
            </NuxtLink>
          </nav>
          <button class="md:hidden text-black">
              <svg class="h-6 w-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
              </svg>
          </button>
      </header>
</template>