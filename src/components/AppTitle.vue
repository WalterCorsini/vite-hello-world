<script>

export default {
  data() {
    return {
      count:0,
      title: "La mia prima app con Vite",
      image: [
        {
          indirizzo: "sfondo-vite.jpg",
        },
        {
          indirizzo: "sfondo-vite-2.jpg",
        },
        {
          indirizzo: "sfondo-vite-3.jpg",
        },
      ],      
    }
  },
  methods:{ 
    createUrlImage(imageName) {
      console.log(imageName.indirizzo);
      console.log(this.image.length);
      return new URL(`../assets/img/${imageName.indirizzo}`, import.meta.url).href;
    },
  },
};
</script>

<template>
    <h1>{{ title }}</h1>
    <img 
    @click="count < image.length-1 ? count++ : count=0"
    :src="createUrlImage(image[count])" />
</template>

<style>
    img{
        width: 70%;
    }
</style>