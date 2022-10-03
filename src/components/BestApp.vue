<template>
    <section class="best-app-area pt-100 fix" :style="bgImg">
        <div class="container">
            <div class="row">
                <div class="col-xl-6 col-lg-6">
                    <div class="bestapp-content-inner text-center">
                        <div class="section-title text-center">
                            <div class="title-icon"></div>
                            <h2 class="title text-white">Finca EL RECUERDO</h2>
                            <p>Fundado por René Aguirre.</p>
                        </div>
                        <div class="bestapp-content-text">
                            <p>La familia Aguirre con mas de 50 años cultivando café.</p>
                            <a href="#" class="read-more active"><i class="fa fa-facebook"></i> Facebook</a>
                            <a href="#" class="read-more"><i class="fa fa-instagram"></i> Instagram</a>
                        </div>
                    </div>
                </div>
                <div class="col-xl-6 col-lg-6">
                    <div class="bestapp-thumb text-end">
                        
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Bestapp',
    props: ["bestappTwo"],
    data (){
        return {
            bgImg: {
                backgroundImage: `url(${require('../assets/img/bestapp-bg.jpg')})`
            }
        }
    }
}
</script>

<style lang='scss'>
    @import '../assets/scss/variables.scss';
    @import '../assets/scss/components/best-app.scss';
</style>
