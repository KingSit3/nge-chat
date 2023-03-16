<template>
  <div class="space-y-3">

    <!-- Room name -->
    <div class="text-center font-semibold text-xl">{{ $route.query?.['room-name'] ?? '???' }}</div>
    <!-- End Room name -->
    
    <!-- Chat Container -->
    <div class="bg-slate-500 text-black rounded-md h-[67vh] mx-40 overflow-y-auto px-5">

      <!-- Chat Card -->
      <div class="space-y-14 first:pt-10 last:pb-10">
        <ChatCard v-for="(item, index) in 5" :key="index" :type="item % 2 == 0 ? 'me' : 'other' " />
      </div>
      <!-- End Chat Card -->

    </div>
    <!-- End Chat Container -->

    <!-- Chat input box -->
    <div class="w-full flex justify-center items-center gap-2">
      <input type="text" v-model="message" class="w-1/2 p-2 bg-slate-300/40 rounded-xl px-2 focus:outline-none outline-none" placeholder="Message">

      <!-- Send Message Button -->
      <button v-if="!sendingMessage" :class="message ? 'text-lime-500 hover:opacity-75 animate-pulse' : 'text-white cursor-default' " class="duration-100">
        <svg viewBox="0 0 24 24" class="w-7 h-7">
          <path d="M21.426 11.095l-17-8A1 1 0 0 0 3.03 4.242l1.212 4.849L12 12l-7.758 2.909l-1.212 4.849a.998.998 0 0 0 1.396 1.147l17-8a1 1 0 0 0 0-1.81z" fill="currentColor"/>
        </svg>
      </button>
      <!-- End Send Message Button -->

      <!-- Sending Icon -->
      <div v-else>
        <svg viewBox="0 0 16 16" class="text-white animate-spin w-7 h-7">
          <path fill="currentColor" d="M8 0A8 8 0 0 0 .002 7.812C.094 4.033 2.968 1 6.5 1C10.09 1 13 4.134 13 8a1.5 1.5 0 0 0 3 0a8 8 0 0 0-8-8zm0 16a8 8 0 0 0 7.998-7.812C15.906 11.967 13.032 15 9.5 15C5.91 15 3 11.866 3 8a1.5 1.5 0 0 0-3 0a8 8 0 0 0 8 8z"/>
        </svg>
      </div>
      <!-- End Sending Icon -->

    </div>
    <!-- End Chat input box -->

  </div>
</template>
<script setup lang="ts">
  import ChatCard from "@/components/ChatCard.vue";
  import { ref } from "vue";

  const message = ref<string>('')
  const sendingMessage = ref<boolean>(false)

</script>