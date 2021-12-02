<template>
  <main>
    <Navigation />
    <Header :pageInfo="siteInfo" />
    <section>
      <h2 class="text-black text-6xl m-10 p-16 text-center">Get In Touch With Us</h2>
    <div class="md:flex md:justify-center mb-6 bg-gray-200">  
      <form class="w-full max-w-lg" action="https://formspree.io/f/xayakjqr" method="POST" id="contact">
    <div class="md:flex md:items-center mb-6">
      <div class="md:w-1/3">
        <label class="block text-gray-500 font-bold md:text-right mb-1 md:mb-0 pr-4" for="name">Your Name</label>
        </div>
      <div class="md:w-2/3">
        <input class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-black" type="text" id="name" name="name" placeholder="Your Name" required>
      </div>
    </div>
    <div class="md:flex md:items-center mb-6">
    <div class="md:w-1/3">
        <label class="block text-gray-500 font-bold md:text-right mb-1 md:mb-0 pr-4" for="email">Your E-mail</label>
        </div>
        <div class="md:w-2/3">
        <input class="bg-gray-200 appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-gray-700 leading-tight focus:outline-none focus:bg-white focus:border-black" type="email" id="email" name="email" placeholder="Your E-mail" required>
        </div>
        </div>
   <div class="md:flex md:items-center mb-6">
    <div class="md:w-1/3">
        <label class="block text-gray-500 font-bold md:text-right mb-1 md:mb-0 pr-4" for="email">Subject</label>
        </div>
        <div class="md:w-2/3">
        <textarea class="form-textarea mt-1 block w-full" id="subject" name="subject" placeholder="Write Subject Here" required></textarea>
        <input class=" appearance-none border-2 border-gray-200 rounded w-full py-2 px-4 text-black bg-white leading-tight focus:outline-none focus:bg-white focus:border-black" type="submit" value="Submit">
        </div>
        </div>
        
       
        
        
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
