<template>
    <div class="album-card">
        <img :src="poster" :alt="title">
        <h3 class="album-title">{{ title }}</h3>
        <div class="album-info">
            <h5 class="album-artist">{{ author }}</h5>
            <h5 class="album-year">{{ year }}</h5>
        </div>

    </div>
</template>
<script>


export default {
    name: 'AlbumCard',
    props: {
        poster: String,
        title: String,
        author: String,
        year: String,


    }
}
</script>
<style lang="scss" scoped>
@import '../assets/sass/_var.scss';

.album-card {

    padding: 15px;
    background-color: $album_bg_color;
    height: 350px;
    text-align: center;

    img {
        margin-bottom: 20px;
    }



    .album-title {
        color: $title_color;
        text-transform: uppercase;
        margin-bottom: 20px;

    }

    .album-info {
        color: $album_info_color ;

        .album-artist {
            font-size: 17px;
        }

    }
}
</style>