<template>
  <div class="text-center flex justify-center p-5 bg-gray-500">
    <figure>
      <h3 class="text-5xl p-2">{{ memberInfo.name }}</h3>
      <a :href="memberInfo.link" target="_blank">
        <nuxt-img class="rounded-full border-solid border-4 border-black" :src="memberInfo.image" sizes="sm:300px md:400px lg:500px" />
      </a>
      <figcaption class="text-3xl"v-text="memberInfo.role" />
    </figure>
  </div>
</template>
<script>
export default {
  props: ["pageInfo", "memberInfo"],
};
</script>