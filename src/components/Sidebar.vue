 <script setup>
 import { defineEmits } from 'vue';//used to declare event and pass event information to parent commponet
 //allows you to declare the events that a component can emit to its parent. It is similar to the props option, but for events.
 //The parent component can then listen to the events using v-on or @ syntax. For example:
//<my-button @click="doSomething"></my-button>
 const emits = defineEmits(['selectOption'])
 const selectOption=(isColor)=>{
 emits("selectOption", isColor)
}
</script>
<template>
    <v-navigation-drawer
        expand-on-hover
         rail>
        <v-list>
        <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            title="Amare Engidawork"
            subtitle="amare_a88@gmailcom"
          >
        </v-list-item>
        </v-list>
        <v-list density="compact" nav>
        <v-list-item 
          prepend-icon="mdi-folder" 
          title="Color Gallery"
          value="Color"
          @click="selectOption(true)"
          />
          <v-list-item 
          prepend-icon="mdi-folder" 
          title="Grayspace Gallery"
          value="Color"
          @click="selectOption(false)"/>
        </v-list>
    </v-navigation-drawer>
    </template>
 