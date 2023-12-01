<template>
  <div class="main">
  <carousel :itemsToShow="1.5">
    <slide v-for="(list, index) in lists" :key="index">
      <img :src="require(`./assets/${list.photo}`)" alt="Slide" />
    </slide>

    <template #addons>
      <navigation />
      <pagination />
    </template>
  </carousel>
</div>
</template>

<script>
import 'vue3-carousel/dist/carousel.css';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';

export default {
  name: 'App',
  components: {
    Carousel,
    Slide,
    Pagination,
    Navigation,
  },
  data() {
    return {
      lists: [
        { photo: '1.jpg' },
        { photo: '2.jpg' },
        { photo: '3.jpg' },
        { photo: '4.jpg' },
        { photo: '5.jpg' },
      ],
    };
  },
};
</script>

<style>
*{
  margin: 0;
  padding: 0;
}
.main{
 padding:120px 100px;
 background-color: burlywood;
}

img {
  width: 500px;
  height: 500px;
  border-radius:10%;
  outline: none;
  border: none;
}
</style>