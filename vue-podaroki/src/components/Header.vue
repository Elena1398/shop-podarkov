<template>
  <header class="flex justify-between border-b border-slate-300 px-10 py-8">
    <div class="flex items-center gap-10">
      <img src="/logo.jpg" alt="logo" class="w-20" style="position: relative; left: 20px" />
      <div>
        <h2 class="text-xl font-bold uppercase">Surprise for you</h2>
        <p class="text-gray-400">Магазин подарков</p>
      </div>
    </div>

    <ul class="flex items-center gap-10">
      <li class="flex items-center cursor-pointer gap-2 text-gray-400 hover:text-black">
        <img src="/cart.svg" alt="cart" class="opacity-50" />
        <span>1500 руб.</span>
      </li>

      <li class="flex items-center cursor-pointer gap-2 text-gray-400 hover:text-black ">
        <img src="/heart.svg" alt="heart" class="opacity-50"/>
        <span>Закладки</span>
      </li>

      <li class="flex items-center cursor-pointer gap-2 text-gray-400 hover:text-black ">
        <img src="/profile.svg" alt="profile" class="opacity-50" />
        <span>Профиль</span>
      </li>
    </ul>
  </header>
</template>
