<template>
  <div>
    <Navigation />
    <Header :pageInfo="siteInfo" :team="team" />
    <main class="flex justify-evenly gap-x-16 gap-y-16 flex-wrap p-16 bg-gray-400">
      <Team :pageInfo="siteInfo" v-for="member in team" :key="member.id" :memberInfo="member" />
    </main>
    <Footer :pageInfo="siteInfo" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      siteInfo: {
        pageName: "Our Team",
        teamName: "FastVue",
      },
      team: [
        {
          name: "name",
          image: "images",
          role: "role",
          link: "url",
        },
        {
          name: "name",
          image: "images",
          role: "role",
          link: "url",
        },
        {
          name: "name",
          image: "images",
          role: "role",
          link: "url",
        },
        {
          name: "name",
          image: "images",
          role: "role",
          link: "url",
        },
      ],
    };
  },
};
</script>