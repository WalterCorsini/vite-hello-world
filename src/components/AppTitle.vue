<script>
export default {
  data() {
    return {
      title: "La mia prima app con Vite",
      image: "sfondo-vite.jpg",
    }
  },
  methods:{ 
    createUrlImage(imageName) {
        return new URL(`../assets/img/${imageName}`, import.meta.url).href;
    },
  },
};
</script>

<template>
    <h1>{{ title }}</h1>
    <img :src="createUrlImage(image)" />
</template>

<style>
    img{
        width: 70%;
    }
</style>