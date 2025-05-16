<script setup>
defineProps(['offerName'])
</script>
<template>
  <div class="wrapper">
    <slot></slot>
    {{ offerName }}
  </div>
</template>
<style scoped>
.wrapper {
  width: 200px;
  height: 300px;
  background: blue;
  color: white;
  border: 1px solid black;
  margin: 10px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
}
</style>
