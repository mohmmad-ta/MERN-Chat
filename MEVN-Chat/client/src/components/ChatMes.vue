<template>
  <div class="backdrop-blur-3xl flex flex-col w-full h-full relative">
    <!--    Navbar   -->
    <div class="flex flex-wrap w-full  gap-2 bg-zinc-900 bg-opacity-70 justify-between py-2 items-center px-5">
      <div class="flex gap-2">
        <img class="rounded-full h-11 w-11 border-2 border-gray-600 p-1" src="@/assets/jj.jpg" alt="">
        <div>
          <h2 class="text-md font-bold text-zinc-200">mohmmad</h2>
          <p class="font-semibold text-sm text-zinc-400">@7md</p>
        </div>
      </div>
      <div class="flex gap-3">
        <i class="fa-solid fa-phone p-2 rounded-full bg-zinc-900 duration-200 text-gray-500 hover:text-gray-200 cursor-pointer"></i>
        <i class="fa-solid fa-video p-2 rounded-full bg-zinc-900 duration-200 text-gray-500 hover:text-gray-200 cursor-pointer"></i>
        <i class="fa-regular fa-bell p-2 rounded-full bg-zinc-900 duration-200 text-gray-500 hover:text-gray-200 cursor-pointer"></i>
        <i class="fa-sharp fa-solid fa-circle-exclamation p-2 rounded-full bg-zinc-900 duration-200 text-gray-500 hover:text-gray-200 cursor-pointer"></i>
      </div>
    </div>
    <!--  Chat Box  -->
    <div class="w-full h-full flex items-end overflow-y-scroll px-4 no-scrollbar">
      <div>
        <div  v-for="message in messages">
          <div class="flex w-full gap-2 h-fit my-2 items-end">
            <img class="rounded-full h-10 w-10 border-2 border-gray-600 p-1" src="@/assets/jj.jpg" alt="">
            <div class="bg-violet-500 rounded-xl px-3 py-1 rounded-bl-sm">
              <p class="font-semibold text-sm text-zinc-100">{{message.mes}}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!--  Input Mes  -->
    <div class="w-full flex items-center h-20 gap-4 px-3 md:px-10">
      <div class="flex gap-2 items-center bg-zinc-900 justify-between w-full rounded-3xl overflow-hidden px-3 my-2 py-1">
        <i class="fa-solid fa-face-smile p-2 rounded-full bg-zinc-900 duration-200 text-gray-500 hover:text-gray-200 cursor-pointer"></i>
        <input class="w-full h-10 outline-none bg-zinc-900 text-zinc-200" type="text" placeholder="Enter your mes">
      </div>
      <i class="fa-solid fa-paper-plane px-3 py-2 text-2xl rounded-full bg-zinc-900 duration-200 text-gray-500 hover:text-violet-500 cursor-pointer"></i>
    </div>
  </div>
</template>

<script setup>
defineProps({
  messages: {
    type: Array
  }
})
</script>