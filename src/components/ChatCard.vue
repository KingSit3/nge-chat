<template>
  <div :class="type == 'me' ? 'flex justify-end' : '' " class="w-full">
    <div :class="type == 'me' ? 'flex-row-reverse' : '' " class="flex gap-2">

      <!-- Profile -->
      <div class="sticky top-3 w-10 h-10">
        <img src="@/assets/images/profile1.png" alt="Profile Image" class="w-10 h-10 rounded-full object-cover border-b-2 border-r-2 border-lime-500">
      </div>
      <!-- End Profile -->

      <!-- Chat Message -->
      <div :class="type == 'me' ? 'border-l-2 ml-20' : ' border-r-2 mr-20' " class="bg-white rounded-lg border-b-2 border-lime-500 w-fit p-2 relative">

        <!-- Kimi no namae wa? -->
        <p :class="type == 'me' ? 'right-2' : 'left-2' " class="absolute -top-7 text-white font-semibold">Udin!!</p>
        <!-- Kimi no namae wa? -->

        <!-- Chat -->
        <h3>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Quasi perferendis id eius sed, officiis facere iure in quo ipsum aliquid quia dignissimos magni iusto sint cum. Lorem ipsum dolor sit amet consectetur adipisicing elit. Quis dolor non modi eius at laboriosam consequatur perspiciatis itaque nobis, voluptas quod cum culpa, repudiandae dolorem mollitia magni delectus cumque consequuntur facere fugiat, officiis facilis tempora iste amet? Quod, non veniam fugit perspiciatis neque hic nam animi, maiores eos consequatur molestias odio laboriosam aut ea assumenda molestiae nihil illum vel nemo! Praesentium obcaecati veritatis corporis dolore, voluptatibus repellendus consequatur facilis nihil nesciunt dolor quos! Voluptatem quae assumenda et ullam at quisquam, corporis amet eveniet doloribus quod modi. Et error, dolore voluptatibus laudantium aliquam officia, reprehenderit adipisci maxime expedita vero inventore, nobis provident voluptas? Dolorum molestias iusto, sit minus deleniti itaque nemo quo corporis quibusdam? Ipsam vel, necessitatibus commodi laudantium neque assumenda culpa velit, exercitationem molestiae recusandae perferendis perspiciatis doloremque cumque facere iusto reprehenderit iste nesciunt quae quos, ea porro aliquam! Sapiente velit consequatur laudantium earum eligendi voluptate similique illo quo perferendis animi, tenetur expedita facilis numquam dolor odit rerum, odio labore culpa aliquid dicta est ratione? Architecto atque vero rem, esse dolor possimus quos incidunt omnis fuga quas voluptatibus iusto numquam fugiat illo ad id ab repellendus minus hic corporis cumque officia quibusdam ratione iure. Ducimus odio molestiae recusandae totam labore fugit sunt esse illo quis eaque consequatur, rerum perferendis possimus facere sapiente necessitatibus voluptatum enim qui quo doloribus, quod sit. Quibusdam doloremque pariatur necessitatibus assumenda eaque earum deserunt, quia unde nisi perspiciatis. Dignissimos ratione soluta doloremque, est necessitatibus asperiores harum sed ex perferendis quidem voluptatum reprehenderit velit dolorem alias ullam quibusdam aspernatur modi, nulla at quas! Ea inventore, iusto velit aspernatur omnis ullam ratione dicta vitae sed vero praesentium deserunt, facere reprehenderit numquam molestiae provident ut, libero pariatur? At eligendi fuga est nobis in assumenda consequatur, necessitatibus repellat dolor impedit architecto optio soluta ducimus a, quibusdam tempora magnam dolorem voluptatibus.</h3>
        <!-- End Chat -->

      </div>
      <!-- End Chat Message -->

    </div>
  </div>
</template>
<script setup lang="ts">
  withDefaults(defineProps<{
    type: 'me' | 'other'
  }>(), {
    type: 'other'
  }) 
</script>