<template>




    <figure class="pb-11 pt-11">
      <h3 class="text-5xl p-2 bg-black text-white">{{ memberInfo.name }}</h3>
      <a :href="memberInfo.link" target="_blank">
        <nuxt-img class="rounded-full border-solid border-4 border-black mt-5 hover:border-pink-600" :src="memberInfo.image" sizes="sm:300px md:300px lg:300px" />
      </a>
      <figcaption class="text-3xl" v-text="memberInfo.role" />
    </figure>

</template>
<script>
export default {
  props: ["pageInfo", "memberInfo"],
};
</script>
