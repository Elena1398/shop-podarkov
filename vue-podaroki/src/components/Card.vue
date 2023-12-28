<script setup>
defineProps({
  title: String,
  imageUrl: String,
  price: Number,
  isFavorite: Boolean,
  isAdded: Boolean,
  onClickAdd: Function,
  onClickFavorite: Function
})
</script>
<template>
  <div
    class="relative border border-slate-100 rounded-xl p-8 cursor-pointer my-element transform transition duration-300 hover:-translate-y-2 hover:shadow-xl"
  >
    <img
      :src="!isFavorite ? '/like-1.svg' : 'like-2.svg'"
      alt="like-1"
      class="absolute top-10 left-10"
      @click="nClickFavorite"
    />

    <img :src="imageUrl" class="w-56" alt="pres" />

    <p class="mt-5">{{ title }}</p>

    <div class="flex justify-between mt-5">
      <div class="flex flex-col">
        <span class="text-gray-400">Цена:</span>
        <b>{{ price }} руб.</b>
      </div>
      <img @click="onClickAdd" :src="!isAdded ? '/plus.svg' : 'check box.svg'" alt="plus" />
    </div>
  </div>
</template>
