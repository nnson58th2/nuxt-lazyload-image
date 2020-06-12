<template>
  <div class="container">
    <h1>Demo Lazyload Image</h1>

    <div class="grid">
      <div
        v-for="(item, index) in lazyImage"
        :key="index"
        class="card"
      >
        <img v-if="index % 2 === 0" v-lazy="require(`~/assets/${item}`)" class="image" />
        <div v-else v-lazy:background-image="require(`~/assets/${item}`)" class="bg bg-image" />
      </div>
    </div>
  </div>
</template>

<script>

export default {
  data() {
    return {
      lazyImage: [
        'image-1.jpg',
        'image-2.png',
        'image-3.png',
        'image-4.png',
        'image-2.png',
        'image-3.png',
        'image-1.jpg',
        'image-1.jpg',
        'image-2.png',
        'image-3.png',
        'image-4.png',
        'image-3.png',
        'image-1.jpg',
        'image-2.png',
        'image-3.png',
        'image-2.png',
        'image-4.png',
        'image-3.png',
        'image-1.jpg',
        'image-1.jpg',
        'image-2.png',
        'image-3.png',
        'image-4.png',
        'image-3.png',
        'image-1.jpg',
        'image-2.png',
        'image-3.png',
        'image-4.png',
        'image-2.png',
        'image-3.png',
        'image-1.jpg',
        'image-1.jpg',
        'image-2.png',
        'image-4.png',
        'image-2.png',
        'image-3.png'
      ]
    };
  }
}
</script>

<style scoped>
  h1 {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    text-align: center;
    margin-bottom: 50px;
  }

  .container {
    max-width: 1456px;
    padding: 0 45px;
    width: 100%;
    margin: 0 auto;
  }

  .grid {
    display: flex;
    flex-wrap: wrap;
    margin-right: -15px;
    margin-left: -15px;
  }

  .card {
    position: relative;
    width: 100%;
    padding-right: 15px;
    padding-left: 15px;
    flex: 0 0 25%;
    max-width: 25%;
    margin-bottom: 50px;
  }

  .image {
    max-width: 100%;
    border: 2px solid orange;
    border-radius: 25px;
    cursor: pointer;
  }

  .bg-image {
    padding-bottom: 42.5%;
    background-color: #fff;
    border: 2px solid orange;
    border-radius: 25px;
    cursor: pointer;
  }

  .bg {
    background-repeat: no-repeat;
    background-position: top;
    background-size: cover;
  }

  /* .lazyload,
  .lazyloading {
    opacity: 0;
  }

  .lazyloaded {
    opacity: 1;
    transition: opacity .4s;
  } */
</style>>
