<script setup>
import Dialpad from './components/Dialpad.vue'

const handleKey = (key) => {
  console.log(key)
}

</script>

<template>
  <div>
    <Dialpad @key="handleKey" />
  </div>
</template>

<style scoped>

</style>
