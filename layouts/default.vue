<template>
<v-app>

    <v-toolbar flat fixed>
      <v-toolbar-side-icon></v-toolbar-side-icon>

      <v-toolbar-title>Title</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>search</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>favorite</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>more_vert</v-icon>
      </v-btn>
    </v-toolbar>

    <div @click="tune">
        <nuxt />
    </div>

</v-app>
</template>

<script>
import VueMoJS from 'vue-mo-js'
import mojs from 'mo-js'
export default {
    data() {
        return {
            icons: [
                'fab fa-facebook',
                'fab fa-twitter',
                'fab fa-google-plus',
                'fab fa-linkedin',
                'fab fa-instagram'
            ],
            clipped: false,
            drawer: true,
            fixed: false,
            items: [{
                    icon: 'apps',
                    title: 'Welcome',
                    to: '/'
                },
                {
                    icon: 'bubble_chart',
                    title: 'Inspire',
                    to: '/inspire'
                }
            ],
            miniVariant: false,
            right: true,
            rightDrawer: false,
            title: 'Vuetify.js',
            OPTS: {
                fill: 'none',
                radius: 55,
                strokeWidth: {
                    50: 0
                },
                scale: {
                    0: 1
                },
                angle: {
                    'rand(-35, -70)': 0
                },
                duration: 1500,
                left: 0,
                top: 0,
                easing: 'cubic.out'
            },
            circle1: undefined,
            circle2: undefined,
            circle3: undefined

        }
    },
    mounted() {
        this.circle1 = new mojs.Shape({
            ...this.OPTS,
            stroke: '#37474F',
        })

        this.circle2 = new mojs.Shape({
            ...this.OPTS,
            radius: {
                1: 15
            },
            strokeWidth: {
                30: 0
            },
            stroke: '#00796B',
            delay: 'rand(75, 150)'
        })

         this.circle3 = new mojs.Shape({
            ...this.OPTS,
             radius: {
                0: 55
            },
            strokeWidth: {
                25: 0
            },
            stroke: '#9FA8DA',
        })
    },

    methods: {
        tune(e) {
            this.circle1
                .tune({
                    x: e.pageX,
                    y: e.pageY
                })
                .replay();

            this.circle2
                .tune({
                    x: e.pageX,
                    y: e.pageY
                })
                .replay();

              this.circle3
                .tune({
                    x: e.pageX,
                    y: e.pageY
                })
                .replay();
        }
    }
}
</script>

<style>
.page-enter-active,
.page-leave-active {
    transition: all 1.5s;
}

.page-enter,
.page-leave-active {
    opacity: 0;
    transform: scale(1);
}

body,
html {
    padding: 0;
}

</style>
