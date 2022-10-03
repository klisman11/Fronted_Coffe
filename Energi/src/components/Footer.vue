<template>
    <footer>
        <div class="footer-main dark-bg section-padding" :class="FooterStyle">
            <div class="container">
                <div class="row">
                    <div class="col-12">
                        <div class="footer-content text-center">
                            <ul class="footer-social-link">
                                <li v-for="(social, socials) in socials" :key="socials">
                                    <a :href="social.link" target="_blank">
                                        <i :class=social.icon></i>
                                    </a>
                                </li>
                            </ul>
                            <h3 class="footer-title">GRACIAS POR VISTARNOS!</h3>
                            <p>Con la mejor calidad de café a nivel mundial.</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <div class="footer-bottom black-bg" :class="FooterStyle">
            <div class="container">
                <div class="row">
                    <div class="col-md-6 order-2 order-md-1">
                        <div class="copyright">
                            <p>&copy; 2022 <b class="text-white">ENERCAF</b> Guatemala <i class="fa fa-heart text-danger"></i> </p>
                        </div>
                    </div>
                    <div class="col-md-6 order-1 order-md-2">
                        <div class="useful-link">
                          
                            <a href="#">Iniciar Sesión</a>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
export default {
    name: 'Footer',
    props: ["FooterStyle"],
    data () {
        return {
            socials: [
                {
                    icon: "fa fa-facebook",
                    link: "https://www.facebook.com/klisoved28/"
                },
                {
                    icon: "fa fa-instagram",
                    link: "https://www.instagram.com/klisman28/"
                }
              
               
            ]
        }
    }
}
</script>

<style lang='scss'>
    @import '../assets/scss/variables.scss';
    @import '../assets/scss/components/footer.scss';
</style>
