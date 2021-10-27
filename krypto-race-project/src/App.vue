<template>
  <v-app>
    <div>
      <v-toolbar flat class="toolbar-gradient">
        <v-toolbar-title><h2>KryptoRacer</h2></v-toolbar-title>
      </v-toolbar>
      <v-toolbar dark flat>
        <v-spacer></v-spacer>

        <v-btn text href="#sobre">
          <span style="color: rgb(255, 166, 0)">Sobre</span>
        </v-btn>
        <v-btn text href="#whitepaper">
          <span style="color: rgb(255, 166, 0)">Whitepaper</span>
        </v-btn>
        <v-btn text href="#tokenomics">
          <span style="color: rgb(255, 166, 0)">Tokenomics</span>
        </v-btn>
        <v-btn text href="#roadmap">
          <span style="color: rgb(255, 166, 0)">Roadmap</span>
        </v-btn>
        <v-btn text href="#nft">
          <span style="color: rgb(255, 166, 0)">NFTs</span>
        </v-btn>
      </v-toolbar>
    </div>
    <Banner />

    <v-main class="dark-secondary-color">
      <section id="sobre">
        <Sobre />
      </section>
      <section id="whitepaper"></section>
      <section id="tokenomics"></section>
      <section id="roadmap"></section>
      <section id="nft">
        <v-row justify="center">
          <v-col>
            <Nft name="Duck" :price="1000" src="static/gltf/Duck.gltf" type="gltf"/>
          </v-col>
          <v-col>
            <Nft name="Three" :price="500" src="static/obj/tree.obj" type="obj"/>
          </v-col>
          <v-col>
            <Nft name="LeePerrySmith" :price="850" src="static/obj/LeePerrySmith.obj" type="obj"/>
          </v-col>
        </v-row>
      </section>
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Sobre from "./views/Sobre/Sobre.vue";
import Nft from "./views/Nft/Nfts.vue";
import Footer from "./components/Footer";
import Banner from "./components/Banner.vue";

export default {
  name: "App",

  components: {
    Sobre,
    Footer,
    Banner,
    Nft,
  },

  data: () => ({}),
};
</script>

<style>
.dark-secondary-color {
  background: #2b2b2b;
}
.dark-primary-color {
  background: #171717;
}
.dark-primary-color-96 {
  background: #171717f5;
}
.toolbar-gradient {
  background: linear-gradient(0deg, rgb(255, 166, 0), rgb(255, 125, 0));
}
* {
  color: white;
}
</style>
