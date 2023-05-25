<template>
<div class="bg-zinc-800 flex-col w-96 flex h-full p-3">
  <div class="flex flex-wrap w-full gap-2 justify-between h-16 items-center">
    <div class="flex gap-2">
      <img class="rounded-full h-11 w-11 border-2 border-green-400 p-1" src="@/assets/jj.jpg" alt="">
      <div>
        <h2 class="text-md font-bold text-zinc-200">mohmmad</h2>
        <p class="font-semibold text-sm text-zinc-400">@7md</p>
      </div>
    </div>
    <i class="fa-regular fa-bell p-2 rounded-full bg-zinc-900 duration-200 text-gray-500 hover:text-gray-200 cursor-pointer"></i>
  </div>
  <div class="flex flex-wrap h-10 items-center bg-zinc-900 justify-between w-full rounded-2xl overflow-hidden px-3 my-2 py-1">
    <i class="fa-solid fa-magnifying-glass cursor-pointer text-gray-400"></i>
    <input class="w-[90%] outline-none bg-zinc-900 text-zinc-200" type="text" placeholder="Search">
  </div>
  <ListFriends :friends="friends" />

</div>
</template>

<script setup>
import ListFriends from "@/components/ListFriends.vue";
import {ref} from "vue";
defineProps({
  friends: {
    type: Array
  }
})
</script>