<script lang="ts" setup>
import { TresCanvas } from '@tresjs/core'
import { OrbitControls } from '@tresjs/cientos'
import { NoToneMapping } from 'three'
import Container from './Container.vue'
import { ref, onMounted } from 'vue'

const show = ref(true)

onMounted(() => {
  console.log('App mounted')
  setTimeout(() => {
    show.value = false
  }, 1000)
})
</script>

<template>
  <TresCanvas :tone-mapping="NoToneMapping">
    <TresPerspectiveCamera />
    <OrbitControls />
    <TresAmbientLight :intensity="1" />
    <TresDirectionalLight :intensity="1" />
    <Container v-if="show" />

  </TresCanvas>
</template>

<style>
html,
body {
  margin: 0;
  padding: 0;
  height: 100%;
  width: 100%;
  background-color: red;
}

#app {
  height: 100%;
  width: 100%;
}
</style>
