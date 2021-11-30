<template>
  <div>
    <figure>
      <h3>{{ memberInfo.name }}</h3>
      <a :href="memberInfo.link" target="_blank">
        <nuxt-img :src="memberInfo.image" sizes="sm:300px md:400px lg:500px" />
      </a>
      <figcaption v-text="memberInfo.role" />
    </figure>
  </div>
</template>
<script>
export default {
  props: ["pageInfo", "memberInfo"],
};
</script>