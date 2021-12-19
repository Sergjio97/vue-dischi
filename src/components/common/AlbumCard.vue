<template>
  <div class="album text-center">
      <img class="py-4 px-2" :src="info.poster" alt="info.title">
      <h3 class="mb-3">{{info.title}}</h3>
      <p>{{info.author}}</p>
      <p class="pb-4">{{info.year}}</p>
  </div>
</template>

<script>
export default {
    name: 'AlbumCard',
    props: {
        info: Object
    }
}
</script>

<style lang='scss' scoped>

img {
    width: 100%;
}

.album {
    text-align: center;

    h3 {
        text-transform: uppercase;
        font-weight: bold;
        color: #fff;
        font-size: 16px;
    }

    p {
        color: #808080;
        font-size: 16px;
    }
}
</style>