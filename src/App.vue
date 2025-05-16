<script setup>
import MyComponent from './components/MyComponent.vue'
import MyComponent2 from './components/MyComponent2.vue'
const offers = [
  {
    id: 1,
    name: 'Велосипед',
  },
  {
    id: 2,
    name: 'Футболка',
  },
]
</script>

<template>
  <!-- <MyComponent offer-name="футболка Димы" /> -->
  <my-component v-for="offer in offers" :offer-name="offer.name" :key="offer.id">
    <div class="color-red">Я в карточке товара</div>
  </my-component>
  <my-component offer-name="Джинсы">
    <div>Я не в цикле</div>
  </my-component>

  <my-component2 offer-name="Джинсы">
    <template #header>
      <div>Я нахожусь в заголовке компонента</div>
    </template>
    <template #footer>
      <div>Я нахожусь в подвале компонента</div>
    </template>
  </my-component2>
</template>

<style scoped>
.color-red {
  color: red;
}
</style>
