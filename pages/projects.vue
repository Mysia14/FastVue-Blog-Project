<template>
  <main>
    <Navigation />
    <Header :pageInfo="siteInfo" />
    <section>
      <figure v-for="project in projects" :key="project.slug">
        <a :href="project.description" target="_blank">
          <nuxt-img :src="project.image" sizes="sm:400px md:600px lg:800px" />
        </a>
        <figcaption>{{ project.title }}</figcaption>
      </figure>
    </section>
    <Footer :pageInfo="siteInfo" />
  </main>
</template>

<script>
export default {
  data() {
    return {
      siteInfo: {
        pageName: "Our Projects",
        author: "FastVue",
      },
    };
  },

  // fetch the data from projects in the content folder
  async asyncData({ $content, error }) {
    try {
      const projects = await $content(`projects`).fetch();
      return {
        projects,
      };
    } catch (error) {
      error("No projects found");
    }
  },
};
</script>