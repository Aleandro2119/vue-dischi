<template>
  <main>
    <div class="container">
      <div class="row">
        <div v-for="element in elements" :key="element.title" class="cols">
          <AlbumCard
            :poster="element.poster"
            :title="element.title"
            :author="element.author"
            :year="element.year"
          />
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import axios from "axios";
import AlbumCard from "./AlbumCard.vue";
export default {
  name: "Main",
  components: {
    AlbumCard,
  },

  data() {
    return {
      elements: [],
    };
  },
  mounted() {
    axios
      .get("https://flynn.boolean.careers/exercises/api/array/music")
      .then((res) => {
        this.elements = res.data.response;
      });
  },
};
</script>

<style land="scss" scoped>
.container {
  width: 900px;
  margin: 0 auto;
}
.cols {
  width: calc(100% / 5);
}
</style>