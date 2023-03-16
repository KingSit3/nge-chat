<template>
  <main>

    <!-- Title Desu~ -->
    <h1 class="text-center text-lg md:text-2xl font-bold font-mono animate-bounce">Pilih Ruangan <s>Curhat</s> Ngobrol</h1>
    <!-- End Title Desu~ -->
    
    <!-- Dungeons -->
    <div class="grid grid-cols-2 md:grid-cols-4 lg:grid-cols-6 gap-5 md:gap-10 my-5 md:my-10">
      <RouterLink :to="{name: 'room', params:{id: index}, query: {'room-name': item}}" v-for="(item, index) in roomName.slice(0, 7)" :key="index" >
        <RoomCard
          :roomName="item"
        />
      </RouterLink>
    </div>
    <!-- End Dungeons -->

  </main>
</template>

<script setup lang="ts">
  import RoomCard from '@/components/RoomCard.vue'
  import roomName from "@/assets/RoomName";
</script>