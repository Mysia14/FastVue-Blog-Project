<template>




    <figure class="">
      <h3 class="text-5xl p-2">{{ memberInfo.name }}</h3>
      <a :href="memberInfo.link" target="_blank">
        <nuxt-img class="rounded-full border-solid border-4 border-black" :src="memberInfo.image" sizes="sm:300px md:300px lg:300px" />
      </a>
      <figcaption class="text-3xl" v-text="memberInfo.role" />
    </figure>

</template>
<script>
export default {
  props: ["pageInfo", "memberInfo"],
};
</script>
