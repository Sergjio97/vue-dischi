<template>
<div class="container-fluid">

    <div class="container mb-5">
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
.col-12, .col-md-2 {
    background-color: #2E3A46;
}
</style>