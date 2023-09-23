<template>
  <header class="py-4">
    <div class="container mx-auto border-b-2 border-black py-2">
      <nav class="flex justify-between items-center">
        <nuxt-link to="/">
          <p class="text-2xl font-bold">1001 startup</p>
        </nuxt-link>
        <ul class="flex space-x-4">
          <li>
            <nuxt-link to="/todo">Todo</nuxt-link>
          </li>
          <li>
            <nuxt-link to="/article">Article</nuxt-link>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>
