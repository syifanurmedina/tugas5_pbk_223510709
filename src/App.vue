<template>
  <q-layout view="hHh lpR fFf">

    <q-header elevated class="bg-purple-3 text-black" height-hint="98">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="./assets/logo_sb.png">
          </q-avatar>
          K-Stuff Quby
        </q-toolbar-title>
      </q-toolbar>

      <q-tabs align="left">
        <q-route-tab to="/page1" label="Home" />
        <q-route-tab to="/page2" label="Catalog" />
        <q-route-tab to="/page3" label="About us" />
      </q-tabs>
    </q-header>

    <q-page-container>
      <div class="q-pa-md row items-start q-gutter-md">
    <q-card class="my-card" flat bordered>
      <q-img
        src="./assets/ea.jpg"/>

      <q-card-section>
        <div class="text-overline text-orange-9"></div>
        <div class="text-h5 q-mt-sm q-mb-xs">Helloww!!!</div>
        <div class="text-caption text-black">
          welcome to my galeri kpop stuff. disini kalian bisa temukan beragam jajanan kpop murah meriah. yuk di check katalog dibawah!!
        </div>
      </q-card-section>

      <q-card-actions>
        <q-btn flat color="primary" label="Buka Setiap hari" />
        <q-btn flat color="secondary" label="Kecuali bangkrut" />

        <q-space />

        <q-btn
          color="grey"
          round
          flat
          dense
          :icon="expanded ? 'keyboard_arrow_up' : 'keyboard_arrow_down'"
          @click="expanded = !expanded"
        />
      </q-card-actions>

      <q-slide-transition>
        <div v-show="expanded">
          <q-separator />
          <q-card-section class="text-subtitle2">
            {{ capt }}
          </q-card-section>
        </div>
      </q-slide-transition>
    </q-card>
  </div>

        <div class="q-pa-md">
    <q-carousel
      arrows
      animated
      v-model="slide"
      height="700px"
    >
      <q-carousel-slide name="satu" img-src="./assets/ls1.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">LightStick Zerobaseone</div>
          <div class="text-subtitle1">Rp 550.000</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="dua" img-src="./assets/ls5.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">LightStick Red Velvet</div>
          <div class="text-subtitle1">Rp 540.000</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="tiga" img-src="./assets/ls10.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">LightStick Twice</div>
          <div class="text-subtitle1">Rp 600.000</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="empat" img-src="./assets/cahol1.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">CardHolder Jaemin Nct</div>
          <div class="text-subtitle1">Rp 100.000</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="lima" img-src="./assets/cahol2.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">CardHolder White</div>
          <div class="text-subtitle1">Rp 200.000</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="enam" img-src="./assets/cahol3.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">CardHolder Flower</div>
          <div class="text-subtitle1">Rp 67.000</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="tujuh" img-src="./assets/kc5.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">KeyChain White</div>
          <div class="text-subtitle1">Rp 35.000</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="delapan" img-src="./assets/kc2.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">KeyChain Jaemin Nct</div>
          <div class="text-subtitle1">Rp 50.000</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="sembilan" img-src="./assets/kc3.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">KeyChain Nct Dream</div>
          <div class="text-subtitle1">Rp 45.000</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="sepuluh" img-src="./assets/kc4.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">KeyChain Hello Kitty</div>
          <div class="text-subtitle1">Rp 40.000</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="sebelas" img-src="./assets/pc1.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">PhotoCard Nct Dream Season's Greating</div>
          <div class="text-subtitle1">Rp 200.000</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide name="duabelas" img-src="./assets/pc2.jpg">
        <div class="absolute-bottom custom-caption">
          <div class="text-h2">PhotoCard Nct Dream ISTJ Introvert Ver</div>
          <div class="text-subtitle1">Rp 250.000</div>
        </div>
      </q-carousel-slide>
    </q-carousel>
  </div>
    </q-page-container>

    <q-footer elevated class="bg-purple-3 text-black">
      <q-toolbar>
        <q-toolbar-title>
          <q-avatar>
            <img src="./assets/logo_sb.png" >
          </q-avatar>
          <div>by @syifanurmedina</div>
        </q-toolbar-title>
      </q-toolbar>
    </q-footer>

  </q-layout>
</template>

<script>
import { ref } from 'vue'

export default {
  setup () {
    return {
      slide: ref('satu'),
      expanded: ref(false),
      capt: 'hubungi kami di @ssyifanm_ jika ada kendala.'
    }
  }
}
</script>

<style lang="sass" scoped>
.custom-caption
  text-align: center
  padding: 12px
  color: white
  background-color: rgba(0, 0, 0, .3)
</style>