<template>
  <div>
    <div>
      <img :src="poster" :alt="author" />
      <h4>{{ title }}</h4>
      <p>{{ author }}</p>
      <p>{{ genre }}</p>
      <p>{{ year }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "AlbumCard",
  props: ["poster", "title", "author", "genre", "year"],
};
</script>

<style>
</style>