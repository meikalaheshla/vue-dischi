<template>
    <header>
        <img src="../assets/img/logo.svg" alt="logo">
    </header>
</template>
<script>
export default {
    name: 'TheHeader',
}
</script>
<style scoped lang="scss">
@import '../assets/sass/_var.scss';

header {
    background-color: $header_bg_color;
    padding: 10px;

    img {
        height: 100px;
        display: block
    }

    ;

}
</style>