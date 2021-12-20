<template>
    <div class="container-fluid py-5 px-5">
        <div class="container">
            <div class="col">
                <SearchBar @change="searchGenre()"/>
            </div>
        </div>

        <div class="container">
            <div class="row d-flex flex-wrap justify-content-center">
                <div class="col-12 m-4 col-md-2 m-md-2 col-xl-2 m-xl-3 d-flex flex-wrap justify-content-center" v-for="(album, index) in albums" :key="index">
                    <AlbumCard :info="album"/>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import axios from 'axios';
import AlbumCard from '../common/AlbumCard.vue';
import SearchBar from '../common/SearchBar.vue'
export default {
    name: 'AlbumList',
    components: {
        AlbumCard,
        SearchBar
    },
    data() {
        return {
            albums: null,
        }
    },
    created() {
        axios.get('https://flynn.boolean.careers/exercises/api/array/music')
        .then((response)=> {
            // handle success
            this.albums = response.data.response;
            console.log(response.data.response);
        })
        .catch(function (error) {
            // handle error
            console.log(error);
        })
    },
    methods: {
        searchGenre(payload) {
            this.selectVal = payload;
        }
    },
    computed: {
        genreFiltered() {
            const arrayFiltered = this.albums.filter( (elm) => {
                return elm.genre.includes.toLowerCase()(this.selectVal.toLowerCase());
            } );

            return arrayFiltered;
        }
    }
}
</script>

<style lang='scss' scoped>
.col-12, .col-md-2 {
    background-color: #2E3A46;
}
</style>