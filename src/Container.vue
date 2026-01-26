<script lang="ts" setup>
import MyObject from './MyObject.vue'
import { onMounted, onUnmounted } from 'vue'

onMounted(() => {
    console.log("Container mounted")
})
onUnmounted(() => {
    console.log("Container onUnmounted")
})
</script>
<template>
    <MyObject />
    <!-- <TresMesh>
        <TresTorusGeometry :args="[1, 0.5, 16, 32]" />
        <TresMeshLambertMaterial :color="'#ff0000'" />
    </TresMesh> -->
</template>