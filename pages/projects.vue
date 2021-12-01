<template>
  <main>
    <Navigation />
    <Header :pageInfo="siteInfo" />
    <section>
    <div class="flex flex-wrap text-center justify-evenly">
      <figure class="p-10" v-for="project in projects" :key="project.slug">
      <figcaption class="text-4xl m-10 bg-black text-white pb-2 ">{{ project.title }}</figcaption>
        <a :href="project.description" target="_blank">
          <nuxt-img :src="project.image" sizes="sm:400px md:600px lg:800px" />
        </a>
      </figure>
      </div>
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