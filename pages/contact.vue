<template>
  <main>
    <Navigation />
    <Header :pageInfo="siteInfo" />
    <section class="p-16 text-center bg-gray-500">
      <h2 class="text-black text-6xl m-10">Get In Touch With Us</h2>
      <div class="flex justify-evenly flex-wrap">
      <form action="https://formspree.io/f/xayakjqr" method="POST" id="contact">
        <label for="name">Your Name</label>
        <input type="text" id="name" name="name" placeholder="Your Name" required>
        <label for="email">Your E-mail</label>
        <input type="email" id="email" name="email" placeholder="Your E-mail" required>
        <label for="subject">Subject</label>
        <textarea id="subject" name="subject" placeholder="Write Subject Here" required></textarea>
        <input type="submit" value="Submit">
      </form>
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
        pageName: "Contact US",
        author: "FastVue",
      },
    };
  },
};
</script>
