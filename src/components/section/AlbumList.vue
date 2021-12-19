<template>
<div class="container-fluid">

    <div class="container">
        <div class="row d-flex flex-wrap justify-content-center">
            <div class="col-12 col-md-2 d-flex flex-wrap justify-content-center">
                <AlbumCard/>
            </div>
        </div>
    </div>

    <div class="container">
        <div class="row d-flex flex-wrap justify-content-center">
            <div class="col-12 col-md-2 d-flex flex-wrap justify-content-center">
                <AlbumCard/>
            </div>
        </div>
    </div>

</div>
</template>

<script>
import AlbumCard from '../common/AlbumCard.vue'
export default {
    name: 'AlbumList',
    components: {
        AlbumCard
    }
}
</script>

<style lang='scss' scoped>
h2 {
    text-align: center;
}
</style>