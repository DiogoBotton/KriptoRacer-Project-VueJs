<template>
  <v-card class="mx-auto" max-width="344" dark outlined>
    <template>
      <model-collada
        v-if="type == 'dae'"
        :backgroundAlpha="0"
        :src="src"
      ></model-collada>
      <model-obj
        v-if="type == 'obj'"
        :backgroundAlpha="0"
        :src="src"
      ></model-obj>
      <model-gltf
        v-if="type == 'gltf'"
        :backgroundAlpha="0"
        :src="src"
      ></model-gltf>
    </template>

    <v-card-title> {{ name }} </v-card-title>

    <v-card-subtitle> {{ price }} BUSD </v-card-subtitle>

    <v-card-actions>
      <v-btn color="orange lighten-2" text> Comprar </v-btn>

      <v-spacer></v-spacer>

      <v-btn icon @click="show = !show">
        <v-icon>{{ show ? "mdi-chevron-up" : "mdi-chevron-down" }}</v-icon>
      </v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text>
          I'm a thing. But, like most politicians, he promised more than he
          could deliver. You won't have time for sleeping, soldier, not with all
          the bed making you'll be doing. Then we'll go with that data file!
          Hey, you add a one and two zeros to that or we walk! You're going to
          do his laundry? I've got to find a way to escape.
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
</template>

<script>
import { ModelGltf, ModelObj, ModelCollada } from "vue-3d-model";
export default {
  data: () => ({
    show: false,
  }),
  props: {
    name: String,
    price: Number,
    src: String,
    type: String,
  },
  components: {
    ModelObj,
    ModelCollada,
    ModelGltf,
  },
};
</script>

<style>
</style>