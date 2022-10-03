<template>
    <section class="team-area pt-100 section-padding fix">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="section-title text-center">
                        <div class="title-icon"></div>
                        <h2 class="title">ENERCAF</h2>
                        <p class="paragraph">Un agradecimiento a todas las personas que forman parte de Finca El Recuerdo, que gracias a ellos somos capaces de llevarte la mejor calidad.</p>
                    </div>
                </div>
            </div>
        </div>

        <div class="team-member-inner" :style="bgImg">
            <div class="container">
                <div class="row">
                    <div class="col-12">
                        <div class="team-content text-center">
                            <p></p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="team-member-slider">
            <div class="container">
                <div class="row">
                    <div class="col-12">
                        <swiper
                            :slides-per-view="3"
                            :speed="1000"
                            :breakpoints="swiperOptions.breakpoints"
                        >
                            <swiper-slide v-for="(team, teams) in teams" :key="teams" class="team-member">
                                <div class="member-thumb">
                                    <img :src="team.thumb" alt="team thumb">
                                    <div class="member-content">
                                        <h6 class="title">{{ team.title }}</h6>
                                        <p class="designation">{{ team.designation }}</p>
                                    </div>
                                </div>
                            </swiper-slide>
                        </swiper>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import { Swiper, SwiperSlide } from 'swiper/vue'

export default {
    name: 'Team',
    components: {
        Swiper,
        SwiperSlide
    },
    data (){
        return {
            swiperOptions: {
                breakpoints: {
                    992:{
                        slidesPerView : 3
                    },

                    480:{
                        slidesPerView : 2
                    },

                    320:{
                        slidesPerView : 1
                    }
                }
            },

            teams: [
                {
                    title: "Flor de café", 
                    designation: "Despues de corte", 
                    thumb: require("../assets/img/team/1.jpg")
                },
                {
                    title: "Flor de café", 
                    designation: "", 
                    thumb: require("../assets/img/team/2.jpg")
                },
                {
                    title: "Pergamino secado a patio", 
                    designation: "", 
                    thumb: require("../assets/img/team/3.jpg")
                },
                {
                    title: "Tom jack", 
                    designation: "SEO Specialist", 
                    thumb: require("../assets/img/team/2.jpg")
                }
            ],
            bgImg: {
                backgroundImage: `url(${require('../assets/img/team-bg.jpg')})`
            }
        }
    }
}
</script>

<style lang="scss">
    @import '../assets/scss/variables.scss';
    @import '../assets/scss/components/team.scss';
</style>
