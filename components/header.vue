<script setup lang="ts">
const props = defineProps({
    title: {
      type: String,
      required: true,
    }
  });
</script>



<template>
    <div class="w-full p-3 bg-slate-800 text-white flex justify-between items-center" style="direction: rtl;">
      <span class="text-lg font-bold"> {{ props.title }} </span>
      <nuxt-link :to="`/`"> بازگشت </nuxt-link>
   </div>

</template>