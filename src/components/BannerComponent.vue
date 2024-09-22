<!-- Banner.vue -->
<template>
    <div class="banner">
      <figure class="image is-16by9">
        <img :src="imageSrc" alt="Banner Image" />
      </figure>
      <div class="banner-text has-text-centered">
        <slot></slot>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'BannerComponent',
    props: {
      imageSrc: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .banner {
    position: relative;
  }
  
  .banner-text {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    font-size: 2em;
  }
  </style>