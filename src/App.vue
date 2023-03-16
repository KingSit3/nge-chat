<template>
  <div class="bg-slate-800 text-slate-100 min-h-screen">

    <Header />

    <main class="mx-5 md:container md:mx-auto py-5 min-h-[75vh]">
      <RouterView />
    </main>

    <Footer />

  </div>
</template>

<script lang="ts" setup>
  import Header from '@/components/TheHeader.vue'
  import Footer from '@/components/TheFooter.vue'

</script>
