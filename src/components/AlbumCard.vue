<template>
  <div>
    <div class="form mt-4">
      <img class="w-100" :src="poster" :alt="author" />
      <h5 class="text-center pt-4 text-white">{{ title }}</h5>
      <p class="text-center m-0 text-secondary">{{ author }}</p>
      <p class="text-center text-secondary mb-4">{{ year }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "AlbumCard",
  props: ["poster", "title", "author", "year"],
};
</script>

<style lang="scss" scoped>
.form {
  background-color: #2e3a46;
  height: 320px;
  padding: 1rem;
}
</style>