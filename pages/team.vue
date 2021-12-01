<template>
  <main>
    <Navigation />
    <Header :pageInfo="siteInfo" />
    
    <section>
    <div class="flex flex-wrap text-center justify-evenly ">
      <Team :pageInfo="siteInfo" v-for="member in team" :key="member.id" :memberInfo="member" />
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
        pageName: "Our Team",
        author: "FastVue",
      },
      team: [
        {
          name: "Fesal Badday",
          image: "/assets/images/fesal.png",
          role: "Backend Dev",
          link: "https://github.com/FesalBadday",
        },
        {
          name: "Evan Burton",
          image: "/assets/images/evanpic.jpg",
          role: "Designer",
          link: "https://github.com/Rankorrdagod",
        },
        {
          name: "Jean Marc",
          image: "/assets/images/Jean-Marc.jpg",
          role: "Frontend Dev",
          link: "https://github.com/QDetective",
        },
        {
          name: "Mysia Santana",
          image: "/assets/images/",
          role: "Content Editor",
          link: "https://github.com/Mysia14",
        },
      ],
    };
  },
};
</script>