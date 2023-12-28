<script setup>
import DrawerHead from './DrawerHead.vue'
import CartListItems from './CartListItems.vue'
</script>

<template>
  <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opacity-70"></div>
  <div class="bg-white w-96 h-full fixed right-0 top-0 z-20 p-10">
    <DrawerHead />

    <CartListItems />

    <div class="flex flex-col gap-4 mt-7">
      <div class="flex gap-2">
        <span>Итого:</span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>1300 руб.</b>
      </div>

      <div class="flex gap-2">
        <span>Доставка:</span>
        <div class="flex-1 border-b border-dashed"></div>
        <b>250 руб.</b>
      </div>

      <button
      disabled=""
      class=" mt-4 transition bg-pink-400 w-full  rounded-xl  py-3 text-white disabled:bg-slate-200 hover:bg-pink-500 active:bg-pink-100 cursor-pointer"
    >
      Оформить заказ
    </button>
    </div>
  </div>
</template>
