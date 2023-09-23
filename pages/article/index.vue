<template>
  <div
    class="container flex md:flex-row flex-col my-16 mx-auto md:px-6 justify-around"
  >
    <nuxt-link
      v-for="(article, index) in articles"
      :key="index"
      :to="`/article/${index + 1}`"
      :article="articles"
      class="hover:shadow-md"
    >
      <div class="flex flex-col flex-wrap p-2">
        <div class="w-full">
          <img
            :src="article.img"
            class="mb-6 w-80 rounded-lg shadow-lg dark:shadow-black/20"
            alt="Avatar"
          />
        </div>

        <div class="w-full text-center">
          <h5 class="mb-6 text-xl font-semibold">{{ article.title }}</h5>
        </div>
      </div>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  data() {
    return {
      articles: [
        {
          title: 'Judul Artikel 1',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat dolor explicabo sint quos exercitationem fugiat reiciendis assumenda. Ad quia veritatis, dolor odit, voluptas numquam modi porro eius reprehenderit ullam tenetur?',
          img: 'https://images.unsplash.com/photo-1649282806617-c51bb282899c?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2070&q=80',
        },
        {
          title: 'Judul Artikel 2',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat dolor explicabo sint quos exercitationem fugiat reiciendis assumenda. Ad quia veritatis, dolor odit, voluptas numquam modi porro eius reprehenderit ullam tenetur?',
          img: 'https://images.unsplash.com/photo-1635732646038-0a1a2fe3f2d6?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1074&q=80',
        },
        {
          title: 'Judul Artikel 3',
          content:
            'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Placeat dolor explicabo sint quos exercitationem fugiat reiciendis assumenda. Ad quia veritatis, dolor odit, voluptas numquam modi porro eius reprehenderit ullam tenetur?',
          img: 'https://images.unsplash.com/photo-1640006807976-a6127e9d6fa0?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1171&q=80',
        },
      ],
    }
  },
}
</script>
