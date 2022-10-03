<template>
    <section class="video-section section-padding pt-100 fix" :style="bgImg">
        <div class="container">
            <div class="row align-items-center">
                <div class="col-lg-6 order-2 order-lg-1">
                    <div class="video-player">
                        <figure class="ratio ratio-16x9">
                            <iframe style="border-radius:12px" src="https://open.spotify.com/embed/show/4WOkXHIkNLEu1GCxDGmFks?utm_source=generator" width="100%" height="352" frameBorder="0" allowfullscreen="" allow="autoplay; clipboard-write; encrypted-media; fullscreen; picture-in-picture" loading="lazy"></iframe>
                        </figure>
                    </div>
                </div>
                <div class="col-lg-6 order-1 order-lg-2">
                    <div class="bestapp-content-inner text-center">
                        <div class="section-title text-center">
                            <div class="title-icon"></div>
                            <h2 class="title text-white">PROCESO DE CAFÉ</h2>
                            <p>Para una buena taza de catación va depender del proceso, desde post cosecha.</p>
                        </div>
                        <div class="bestapp-content-text pb-0">
                            <p>Algunos de los tips es para mejora de productividad y calidad.</p>
                            <ul class="video-list">
                                <li> <i class="fa fa-check-square-o"></i> La fermentación</li>
                                <li> <i class="fa fa-check-square-o"></i> Selección de grano</li>


                            </ul>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
    export default {
        name: 'Video',
        data () {
            return {
                bgImg: {
                    backgroundImage: `url(${require('../assets/img/video-bg.jpg')})`
                }
            }
        }
    }
</script>

<style lang='scss'>
    @import '../assets/scss/variables.scss';
    @import '../assets/scss/components/video.scss';
</style>
