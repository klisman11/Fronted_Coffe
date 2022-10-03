<template>
    <section class="about-area section-padding section" id="about" :class="AboutStyle">
        <div class="container">
            <div class="row mtn-30">
                <!-- single item start -->
                <div v-for="(about, abouts) in abouts" :key="abouts" class="col-lg-3 col-md-6">
                    <div class="about-item">
                        <div class="about-icon">
                            <i :class="about.icon"></i>
                        </div>
                        <div class="about-content">
                            <h6>{{ about.title }}</h6>
                            <p>{{ about.desc }}</p>
                        </div>
                    </div>
                </div>
                <!-- single item end -->
            </div>
        </div>
    </section>
</template>

<script>

export default {
    name: 'About',
    props: ["AboutStyle"],
    data (){
        return {
             abouts:[
                { 
                    title: "ARABICA TÍPICA", 
                    desc: "Uno de los cafés más importantes cultural y genéticamente de C. arabica en el mundo, con alta calidad en Centroamérica. ", 
                    icon: "fa fa-pagelines"
                },
                {
                    title: "BOURBOUN", 
                    desc: "Uno de los cafés más importantes cultural y genéticamente de C. arabica en el mundo, conocidos por su excelente calidad de la bebida en las mayores altitudes.", 
                    icon: "fa fa-pagelines"
                },
                {
                    title: "GEISHA", 
                    desc: "En la taza, el Geisha Esmeralda despliega una agradable dulzura, claridad y un sabor brillante que puede variar desde bayas, cítricos, mango, papaya, melocotón, piña, guayaba, y jasmín. ", 
                    icon: "fa fa-pagelines"
                },
                {
                    title: "CATURRA", 
                    desc: "Una planta compacta con un buen potencial de rendimiento y de calidad estándar en Centroamérica.", 
                    icon: "fa fa-pagelines"
                }
            ]
        }
    }
}
</script>

<style lang="scss">
    @import '../assets/scss/variables.scss';
    @import '../assets/scss/components/about.scss';
</style>
