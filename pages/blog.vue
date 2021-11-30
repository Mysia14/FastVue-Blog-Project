<template>
  <v-main>
    <Navigation />
    <Header :pageInfo="siteInfo" />
    <section>
      <h2>{{ post.title }}</h2>
      <nuxt-content :document="post" />
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