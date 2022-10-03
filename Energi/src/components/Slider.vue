<template>
    <section class="slider-section hero-style-1 section" id="home" :style="bgImg">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <swiper
                        :slides-per-view="1"
                        :space-between="30"
                        :speed="1000"
                        :pagination="swiperOptions.pagination"
                    >
                        <swiper-slide v-for="(slider, sliders) in sliders" :key="sliders" class="hero-slider-item">
                            <div class="row align-items-center">
                                <div class="col-xl-6 col-lg-5 col-md-5">
                                    <div class="slider-thumb">
                                        <img :src="slider.sliderThumb" alt="slider thumb">
                                    </div>
                                </div>
                                <div class="col-xl-6 col-lg-7 col-md-7">
                                    <div class="slider-content">
                                        <h2 class="slider-title">{{ slider.sliderTitle }}</h2>
                                        <p class="slider-desc">{{ slider.sliderDesc }}</p>
                                        <div class="slider-btn">
                                            <a href="#" class="read-more active"><i class="fa fa-facebook"></i> Facebook</a>
                                            <a href="#" class="read-more"><i class="fa fa-instagram"></i> Instagram</a>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </swiper-slide>
                        <div class="swiper-pagination pagination-dot-style pagination-dot-style__2"></div>
                    </swiper>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
        import SwiperCore, { Pagination } from 'swiper/core'
        import { Swiper, SwiperSlide } from 'swiper/vue'
        SwiperCore.use([Pagination])

    export default {
        components: {
            Swiper,
            SwiperSlide
        },
        data (){
            return {
                bgImg: {
                    backgroundImage: `url(${require('../assets/img/home-bg.jpg')})`
                },
                sliders: [
                    {
                        sliderThumb: require("../assets/img/slider/home2-slide1.png"), 
                        sliderTitle: 'FINCA EL RECUERDO', 
                        sliderDesc: 'Logrando tener una alta taza de calidad'
                    },
                    {
                        sliderThumb: require("../assets/img/slider/home2-slide1.png"), 
                        sliderTitle: 'ENERCAF',
                        sliderDesc: 'Con nuestras mejores variedades, Geisha,Arabigo, Bourboun'
                    },
                    {
                        sliderThumb: require("../assets/img/slider/home2-slide1.png"), 
                        sliderTitle: 'HUEHUETENANGO', 
                        sliderDesc: 'Elaboramos con el mejor proceso'
                    },
                ],

                swiperOptions: {
                    pagination: {
                        el: '.pagination-dot-style',
                        type: 'bullets',
                        clickable: true
                    }
                }
            }
        }
    }
</script>
