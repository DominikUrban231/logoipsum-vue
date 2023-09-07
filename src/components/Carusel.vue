<template>
    <div class="carusel">
        <swiper
        :slidesPerView="auto"
        :spaceBetween="30"
        :centeredSlides="true"
        :navigation="true"
        :pagination="{
        clickable: true,
        }"
        :modules="modules"
        class="mySwiper"
    >
        <swiper-slide><img src="./../assets/img/gallery-1.jpg" alt=""></swiper-slide>
        <swiper-slide><img src="./../assets/img/gallery-2.jpg" alt=""></swiper-slide>
        <swiper-slide><img src="./../assets/img/gallery-3.jpg" alt=""></swiper-slide>
        <swiper-slide><img src="./../assets/img/gallery-4.jpg" alt=""></swiper-slide>
    </swiper>

    </div>
</template>

<script>
// Import Swiper Vue.js components
import { Swiper, SwiperSlide } from 'swiper/vue';
import 'swiper/css';
import 'swiper/css/navigation';
import 'swiper/css/pagination';
    
// import required modules
import { Pagination, Navigation } from 'swiper/modules';

export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        return {
            modules: [Pagination, Navigation],
        };
    },
};
</script>

<style lang="scss">
.carusel {
    position: relative;;
}
.swiper-button-next {
    color: #FF4359;
}
.swiper-button-prev {
    color: #FF4359;
}
.swiper-button-disabled {
    color: #AFAFAF;
}
.swiper {
    width: 100%;
    height: 100%;
}
.swiper-wrapper {
    height: 70vh;
    .swiper-slide {
        width: 70vw ;
    }
}
.swiper-slide img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}
.swiper-pagination {
    padding-block: 10px;
    position: static;
    display: flex;
    align-items: center;
    justify-content: center;
    .swiper-pagination-bullet-active {
        background-color: #FF4359;
        width: 0.8rem;
        height: 0.8rem;
        ;
    }
}
</style>