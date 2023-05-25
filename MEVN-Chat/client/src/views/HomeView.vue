<template>
  <main>
    <img class="w-full z-[1] h-screen bg-cover absolute" src="@/assets/jj.jpg" alt="">
    <div class="w-full h-screen absolute z-[2]">
      <div class="w-full h-full bg-zinc-900 bg-opacity-70 flex overflow-hidden">
        <AsideChat :friends="friends" />
        <ChatMes :messages="messages" />
      </div>
    </div>
  </main>
</template>

<script setup>
import AsideChat from "@/components/AsideChat.vue";
import ChatMes from "@/components/ChatMes.vue";
import {ref} from "vue";
const friends = ref([
  {
    name: 'mohammed',
    id: '@m7md'
  },
  {
    name: 'ali',
    id: '@ali232'
  },
])
const messages = ref([
  {
    mes: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam aperiam, asperiores blanditiis culpa distinctio earum exercitationem facere illum laboriosam maiores nihil omnis perspiciatis quia recusandae reiciendis similique ut veritatis, voluptatibus?'
  },
  {
    mes: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam aperiam, asperiores blanditiis culpa distinctio earum exercitationem facere illum laboriosam maiores nihil omnis perspiciatis quia recusandae reiciendis similique ut veritatis, voluptatibus?'
  },
  {
    mes: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam aperiam, asperiores blanditiis culpa distinctio earum exercitationem facere illum laboriosam maiores nihil omnis perspiciatis quia recusandae reiciendis similique ut veritatis, voluptatibus?'
  },
])

</script>