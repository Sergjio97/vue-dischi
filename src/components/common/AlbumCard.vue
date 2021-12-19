<template>
  <div class="album text-center">
      <img class="py-4 px-2" src="https://www.onstageweb.com/wp-content/uploads/2018/09/bon-jovi-new-jersey.jpg" alt="">
      <h3 class="mb-3">New Jersey</h3>
      <p>Bon Jovi</p>
      <p class="pb-4">1988</p>
  </div>
</template>

<script>
export default {
    name: 'AlbumCard'
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
    }

    p {
        color: #808080;
        font-size: 20px;
    }
}

</style>