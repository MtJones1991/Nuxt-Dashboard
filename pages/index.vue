<template>
<div class="mb-5">
    <v-parallax height="100%" class="paraImg mb-5" src="https://images.unsplash.com/photo-1497366216548-37526070297c?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1050&q=80https://images.unsplash.com/photo-1497366811353-6870744d04b2?ixlib=rb-1.2.1&auto=format&fit=crop&w=1050&q=80">
        <v-layout align-end justify-start column fill-height>
            <img class=" mr-5 imgFile" src="~/assets/rocket.png" data-aos="fade" data-aos-duration="2000" data-aos-mirror="true" wrap data-aos-easing="ease-in-out">
        </v-layout>

            <v-layout align-center justify-start column fill-height>
                <h1 data-aos="fade" data-aos-duration="2000" data-aos-mirror="true" wrap data-aos-easing="ease-in-out" class="mb-1 text-xs-center siteHeader">How can we help you and your business</h1>
                <p data-aos="fade" data-aos-duration="2000" data-aos-mirror="true" wrap data-aos-easing="ease-in-out" class="mb-1 text-xs-center">Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
                    Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
                    Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum t</p>
            </v-layout>
    </v-parallax>

    <v-layout align-center justify-center column fill-height wrap>
        <h1 data-aos="fade" data-aos-duration="2000" data-aos-mirror="true" wrap data-aos-easing="ease-in-out" class="mt-5 titleTop text-xs-center">A Premier remote experience</h1>
    </v-layout>


    <v-layout align-center justify-center column fill-height wrap>
        <p data-aos="fade" data-aos-duration="2000" data-aos-mirror="true" wrap data-aos-easing="ease-in-out" class="mb-5 text-xs-center">Cras facilisis mi vitae nunc lobortis pharetra. Nulla volutpat tincidunt ornare.
            Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.
            Nullam in aliquet odio. Aliquam eu est vitae tellus bibendum t</p>
    </v-layout>

    <v-layout class="mt-5" align-center justify-center column fill-height wrap>
        <h1 data-aos="fade" data-aos-duration="2000" data-aos-mirror="true" wrap data-aos-easing="ease-in-out" class="mt-5 titleTop text-xs-center">Meet the team</h1>
    </v-layout>

    <v-spacer class="mt-5"></v-spacer>

    <v-layout align-center justify-space-around row fill-height wrap>
        <v-card data-aos="zoom-in-down" data-aos-duration="1900" data-aos-mirror="true" data-aos-anchor-placement="top-center" class=" mb-3 cards text-xs-center">
            <v-img class="cardImg" src="https://images.unsplash.com/photo-1545873446-11013269cbc7?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=334&q=80" height="150px">
            </v-img>

            <v-card-title primary-title>
                <div>
                    <div class="headline text-xs-center">John Doe</div>
                    <span class="grey--text text-xs-center"> Aliquam eu est vitae tellus bibendum</span>
                </div>
            </v-card-title>
        </v-card>

        <v-card data-aos="zoom-out-left" data-aos-duration="2100" data-aos-mirror="true" data-aos-anchor-placement="top-center" class="mb-3 cards text-xs-center">
            <v-img class="cardImg elevation-13" src="https://images.unsplash.com/photo-1507399076055-c021699485c3?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=966&q=80" height="150px">
            </v-img>

            <v-card-title primary-title>
                <div>
                    <div class="headline text-xs-center">Myke Hamel</div>
                    <span class="grey--text text-xs-center">habitant morbi tristique sen</span>
                </div>
            </v-card-title>
        </v-card>

        <v-card data-aos="zoom-out-up" data-aos-duration="2700" data-aos-mirror="true" data-aos-anchor-placement="top-center" class="mb-3 cards text-xs-center">
            <v-img class="cardImg elevation-13" src="https://images.unsplash.com/photo-1527153907022-465ee4752fdc?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1000&q=80" height="150px">
            </v-img>

            <v-card-title primary-title>
                <div>
                    <div class="headline text-xs-center">The Juniors</div>
                    <span class="grey--text text-xs-center">ntesque habitant morbi tristiq</span>
                </div>
            </v-card-title>
        </v-card>

    </v-layout>

    <AboutCards />

    <v-parallax class="paraImg elevation-21 mb-5 mt-5" src="https://picsum.photos/1080/720?image=171">
        <v-layout align-center justify-center column fill-height class="pb-5 mb-5">
            <h4 class="display-1 pt-5 mt-5" color="white" data-aos="zoom-in" data-aos-duration="2100" data-aos-mirror="true">
                <nuxt-link class="inspire" to="/inspire">Inspire</nuxt-link>
            </h4>
        </v-layout>
    </v-parallax>

    <BottomNav />

</div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'
import BottomNav from '~/components/BottomNav.vue'
import AboutCards from '~/components/AboutCards.vue'
export default {
    components: {
        Logo,
        VuetifyLogo,
        BottomNav,
        AboutCards
    },
    data: () => ({
        show: false
    })
}
</script>

<style>
element.style {
    height: 500px;
}

.titleTop {
    color: black;
}

.v-parallax {
    height: 700px !important;
    width: 100%;
    margin-top: 25px;
}

.inspire {
    color: whitesmoke;
    margin-top: 10px;
    text-decoration: none;
    font-family: 'Montserrat' !important;
}

.siteHeader {
    color: whitesmoke;
    margin-top: 10px;
    text-decoration: none;
    font-family: 'Montserrat' !important;
}

.headlineTitle {
    /* border-radius: 50%; */
    background-color: brown;
}

.cards {
    border-radius: 100%;
    background-color: transparent !important;
    border: none !important;
}

.v-card {
    box-shadow: none !important;
    text-align: center;
}

.cardImg {
    width: 150px;
    display: inline-block;
    border-radius: 100%;
}

.headline {
    font-family: 'Montserrat' !important;
}

.inspire {
    padding-bottom: 250px;
    margin-bottom: 205px;
}

.imgFile {
    margin-top: 130px;
    height: 145px;
    width: 145px;
    border-radius: 100%
}
</style>
