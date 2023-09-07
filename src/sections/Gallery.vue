<template>
    <section id="gallery" class="gallery">
        <h1 class="red">GALERIA</h1>
        <Carusel />
    </section>
</template>

<script>
import Carusel from '@/components/Carusel.vue';

export default {
    components: { Carusel }
}
</script>

<style lang="scss">
.gallery {
    margin-top: 8vh;
}
.red {
    max-width: fit-content;
    border-bottom: 2px solid #FF4359;
    margin: auto;
    margin-bottom: 25px;
    padding: 15px;
}
</style>