<template>
  <div>
    <TheHeader />
    <main>
      <AlbumSection />

    </main>

  </div>
</template>

<script>
import TheHeader from './components/TheHeader.vue';
import AlbumSection from './components/AlbumSection.vue';


export default {
  name: 'App',
  components: {
    TheHeader,
    AlbumSection
  }
}
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
</style>
