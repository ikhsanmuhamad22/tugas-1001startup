<template>
  <header class="py-4">
      <div class="container mx-auto border-b-2 border-black py-2">
          <nav class="flex justify-between items-center">
            <nuxt-link to="/">
                <p class="text-2xl font-bold">1001 startup</p>
            </nuxt-link>
              <ul class="flex space-x-4">
                <nuxt-link to="/todo">
                  <li><a href="#" class="">Todo</a></li>
                </nuxt-link>
              </ul>
          </nav>
      </div>
  </header>
</template>