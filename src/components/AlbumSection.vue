<template>
    <section id="albums">
        <div class="albums-list container">
            <div class="album-col" v-for="(album, i) in albums" :key="i">

                <AlbumCard :poster="album.poster" :title="album.title" :author="album.author" :year="album.year" />


            </div>
        </div>
    </section>
</template>
<script>
import axios from 'axios'
import AlbumCard from './AlbumCard.vue';

export default {
    name: 'AlbumSection',
    components: {
        AlbumCard
    },
    data() {
        return {

            albums: [],
        }
    },
    mounted() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((res) => {

            this.albums = res.data.response;
            console.log(this.albums)
        });
    }
}
</script>
<style lang="scss" scoped>
@import "../assets/sass/_var.scss";

#albums {
    background-color: $section_bg_color;
    ;

    .albums-list {
        padding-top: 50px;
        padding-bottom: 65px;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        gap: 30px;

        .album-col {

            width: 15%;

        }
    }

}
</style>