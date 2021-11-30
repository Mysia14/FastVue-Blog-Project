<template>
  <main>
    <Navigation />
    <Header :pageInfo="siteInfo" />
    
    <Footer :pageInfo="siteInfo" />
  </main>
</template>

<script>
export default {
  data() {
    return {
      siteInfo: {
        pageName: "Home",
        author: "FastVue",
      },
    };
  },
};
</script>
