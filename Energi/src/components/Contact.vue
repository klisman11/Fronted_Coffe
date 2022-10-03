<template>
    <section class="contact-area section-padding pt-100 fix section" :style="bgImg" :class="ContactStyle" id="support">
        <div class="container">
            <div class="row">
                <div class="col-12">
                    <div class="section-title text-center" :class="['title-style-2 title-line-2', ContactStyle]">
                        <div class="title-icon" ></div>
                        <h2 class="title">CONTACTO</h2>
                        <p class="paragraph">Si tienes dudas puedes escribirnos</p>
                    </div>
                </div>
            </div>
            <div class="row support-container">
                <div class="col-md-8">
                    <form action="#" class="support-form">
                        <div class="input-box">
                            <input class="text-field" type="text" name="name" placeholder="Nombre" />
                        </div>
                        <div class="input-box">
                            <input class="text-field" type="email" name="email" placeholder="Correo Electrónico" />
                        </div>
                        <div class="input-box">
                            <textarea class="text-field" name="message"  placeholder="Mensaje" ></textarea>
                        </div>
                        <div class="input-box">
                            <input class="btn-submit" type="submit" value="ENVIAR" />
                        </div>
                    </form>
                </div>
                <div class="col-md-4">
                    <div class="support-info text-center">
                        <div class="single-info">	
                            <div class="icon">
                                <i class="fa fa-phone"></i>
                                </div>
                            <h6 class="support-title">Telefono</h6>
                            <p>(+502)58694011</p>
                        </div>
                        <div class="single-info">	
                            <div class="icon">
                                <i class="fa fa-envelope-open-o "></i>
                                </div>
                            <h6 class="support-title">Correo Electrónico</h6>
                            <p>klisoved28@gmail.com</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Contact',
    props: ["ContactStyle"],
    data (){
        return {
            bgImg: {
                backgroundImage: `url(${require('../assets/img/support-bg.jpg')})`
            }
        }
    }
}
</script>

<style lang='scss'>
    @import '../assets/scss/variables.scss';
    @import '../assets/scss/components/contact.scss';
</style>
