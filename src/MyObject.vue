<script lang="ts" setup>
import { Plane } from '@tresjs/cientos'
import { onMounted, onUnmounted } from 'vue'

onMounted(() => {
    console.log('MyTorus mounted')
})

onUnmounted(() => {
    console.log('MyTorus unmounted')
})
</script>

<template>

    <TresMesh>
        <TresTorusGeometry :args="[1, 0.5, 16, 32]" />
        <TresMeshLambertMaterial :color="'#ff0000'" />
    </TresMesh>
    <!-- <Plane :args="[10, 10]"
        :position="[0,0,0]" :receive-shadow="true">
        <TresMeshLambertMaterial ref="materials" :color="'#809966'" />
    </Plane> -->
</template>
