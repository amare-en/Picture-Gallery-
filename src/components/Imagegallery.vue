<script setup>
import { defineProps } from 'vue';
const A = defineProps(["isWithColor"])
</script>
<template>
      <v-row class="ma-10">
       <v-col
        v-for="n in 100"
        :key="n"
        cols=""
           >
  <v-cards :elevation="isHovering ? 12:2"
  v-bind="$props">
  <v-img
     :width="300"
     aspect-ratio="1"
     cover
     :src="`https://picsum.photos/500/300?image=${n * 5 + 10} ${A.isWithColor? '': '&grayscale'}`"
     :lazy-src="`https://picsum.photos/10/6?image=${n * 5 + 10} ${A.isWithColor? '':'&grayscale'}`"
></v-img>
</v-cards>
</v-col>   
</v-row>
</template>   