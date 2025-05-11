<script setup lang="ts">
const props = defineProps({
    id: {
      type: Number,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    leader: {
      type: String,
      required: true,
    },
    expireDate: {
      type: String,
      required: true,
    },
  });
</script>



<template>
<nuxt-link :to="`/detail/${props.id}`">
    <div class="w-full rounded-lg p-3 bg-slate-800 text-white flex flex-col" style="direction: rtl;">
    <span class="text-lg font-bold"> {{ props.title }} </span>
    <div class="flex justify-between text-xs mt-2">
        <span> {{ props.leader }}</span>
        <span> {{ props.expireDate }} </span>
    </div>
   </div>
</nuxt-link>
</template>