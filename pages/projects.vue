<template>
  <main>
    <Navigation />
    <section>
      <figure v-for="project in projects" :key="project.slug">
        <a :href="project.description" target="_blank">
          <nuxt-img :src="project.image" sizes="sm:400px md:600px lg:800px" />
        </a>
        <figcaption>{{ project.title }}</figcaption>
      </figure>
    </section>
  </main>
</template>

<script>
export default {
  // fetch the data from the blog in the content folder
  async asyncData({ $content }) {
    const projects = await $content("projects").fetch();
    return {
      projects,
    };
  },
};
</script>