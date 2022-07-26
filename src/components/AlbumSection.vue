<template>
    <section id="albums">
        <AlbumCard />
    </section>
</template>
<script>
import axios from 'axios'
import AlbumCard from "./AlbumCard.vue";
export default {
    name: 'AlbumSection',
    components: {
        AlbumCard,

    },
    monted() {
        axios.get("https://flynn.boolean.careers/exercises/api/array/music").then((res) => {

        });
    }
}
</script>
<style lang="scss" scoped>
@import "../assets/sass/_var.scss";

#album-section {
    background-color: $section_bg_color;

}
</style>