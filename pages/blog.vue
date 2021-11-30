<template>
  <v-main>
    <Navigation />
    <Header :pageInfo="siteInfo" />
    <section class="flex flex-col text-center bg-gray-500">
      <h2 class="text-4xl m-5">{{ post.title }}</h2>
      <nuxt-content class="text-justify ml-10 mr-10 mb-10 bg-white bg-opacity-50 p-5" :document="post" />
    </section>
    <Footer :pageInfo="siteInfo" />
  </v-main>
</template>
<script>
export default {
  data() {
    return {
      siteInfo: {
        pageName: "Blog",
        author: "FastVue",
      },
    };
  },

  // fetch the data from blog in the content folder
  async asyncData({ $content, params, error }) {
    try {
      const post = await $content(`blog/2021-11-26-nuxt-js`).fetch();
      return {
        post,
      };
    } catch (error) {
      error("No article found");
    }
  },
};
</script>