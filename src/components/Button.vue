<script setup>
import { defineProps } from 'vue';
const props = defineProps(["color"])
</script>
<template>{{ props.color }}
<v-btn density="compact" 
:color="props.color ? 'green' :'yellow'"
>
welcome to ......
</v-btn>
</template>