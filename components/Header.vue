<template>
  <header class="bg-black p-4">
    <h1 class="text-6xl text-center text-white">{{ pageInfo.pageName }}</h1>
  </header>
</template>
<script>
export default {
  props: ["pageInfo"],
};
</script>