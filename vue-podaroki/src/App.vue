<script setup>
import { onMounted, ref } from 'vue'
import axios from 'axios'

import Header from './components/Header.vue'
import CartList from './components/CartList.vue'
import Drawer2 from './components/Drawer2.vue'

const items = ref([])

onMounted(async () => {
  try {
    const { data } = await axios.get('https://22aef63578b06b41.mokky.dev/presents')

    items.value = data
  } catch (err) {
    console.log(err)
  }
})
</script>

<template>
  <!--<Drawer2 />-->

  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-20">
    <Header />

    <div class="p-10">
      <div class="flex justify-between items-center">
        <h2 class="text-2xl font-bold mb-8">Все подарки</h2>
        <div class="flex gap-5">
          <select @change="onChangeSelect" class="py-2 px-3 border rounded-md outline-none">
            <option value="name">По названию</option>
            <option value="price">По цене (дешевые)</option>
            <option value="-price">По цене (дорогие)</option>
          </select>

          <div class="relative">
            <img class="absolute left-4 top-3" src="/search.svg" />
            <input
              class="border ronded-md py-2 pl-11 pr-4 outline-none focus:border-gray-400"
              type="text"
              placeholder="Поиск..."
            />
          </div>
        </div>
      </div>

      <div class="mt-10">
        <CartList :items="items" />
      </div>
    </div>
  </div>
</template>

<style></style>
