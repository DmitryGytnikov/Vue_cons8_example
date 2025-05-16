<script setup>
defineProps(['offerName'])
</script>
<template>
  <div class="wrapper">
    <div class="div1">
      text
      <slot name="header"></slot>
    </div>
    <div>zxzxzxzx</div>
    <div>xzxzxzxz</div>
    <div class="div2">
      text2
      <slot name="footer"></slot>
    </div>
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

.div1 {
  background: red;
}

.div2 {
  background: yellow;
  color: black;
}
</style>
