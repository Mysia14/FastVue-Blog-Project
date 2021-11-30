<template>
  <footer class="flex justify-center bg-black text-white p-6 gap-x-1">
    <p>&copy; {{ pageInfo.author }} {{ new Date().getFullYear() }}</p>
  </footer>
</template>
<script>
export default {
  props: ["pageInfo"],
};
</script>