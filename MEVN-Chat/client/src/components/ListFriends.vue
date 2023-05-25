<template>
  <div class="bg-zinc-900 w-full h-full rounded-md overflow-hidden">
    <div class="flex w-full gap-2 justify-around h-fit items-center mt-1 mb-4">
      <button class="text-sm font-semibold text-zinc-300 border-b-2 border-zinc-300 px-3 py-1">All</button>
      <button class="text-sm font-semibold text-zinc-300 border-b-2 border-zinc-300 px-3 py-1">My friends</button>
    </div>
    <div class="overflow-y-scroll no-scrollbar h-full px-2">
      <div v-for="friend in friends">
        <div class="flex flex-wrap w-full gap-2 justify-between h-16 items-center">
          <div class="flex gap-2">
            <img class="rounded-full h-10 w-10 border-2 border-green-400 p-1" src="@/assets/jj.jpg" alt="">
            <div>
              <h2 class="text-sm font-bold text-zinc-200">{{friend.name}}</h2>
              <p class="text-xs text-zinc-400">Lorem ipsum dolor</p>
            </div>
          </div>
          <span class="text-zinc-500 text-xs">1:20 am</span>
        </div>
      </div>

    </div>
  </div>
</template>

<script setup>
defineProps({
  friends: {
    type: Array
  }
})
</script>