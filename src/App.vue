
<script setup>
import Imagegallery from "./components/Imagegallery.vue";
import Button from "./components/Button.vue"
import Sidebar from "./components/Sidebar.vue";
import {ref} from "vue" 
const color=ref(false)
const isWithColor=ref(true)
const onSelectOption=(isColor)=>{
isWithColor.value=isColor
color.value=isColor
} 
</script>
<template>
<v-app>
<Button :color="color"/>
<Sidebar @selectOption="onSelectOption"/>
<Imagegallery :isWithColor="isWithColor"/>
</v-app>
</template>

 