<template>
  <div>
    <h1>Original</h1>
    <nuxt-img
      src="/images/colors.jpg"
      width="500"
      height="500"
      @load="isLoadedRoot = true"
    />
    <p>Received onLoad event: {{ isLoadedRoot }}</p>

    <h1>Layer</h1>
    <nuxt-img
      src="/images/colors-layer.jpg"
      width="500"
      height="500"
      @load="isLoadedLayer = true"
    />
    <p>Received onLoad event: {{ isLoadedLayer }}</p>

    <h1>Layer with dir config</h1>
    <nuxt-img
      src="/images/colors-layer-config.jpg"
      width="500"
      height="500"
      @load="isLoadedLayerWithConfig = true"
    />
    <p>Received onLoad event: {{ isLoadedLayerWithConfig }}</p>
  </div>
</template>

<script setup lang="ts">
import { ref } from '#imports'

const isLoadedRoot = ref(false)
const isLoadedLayer = ref(false)
const isLoadedLayerWithConfig = ref(false)
</script>
