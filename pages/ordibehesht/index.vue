<template>
  <div class="flex flex-col" style="direction: rtl;">
    <Header title="صفحه مدیریت" />
    <div class=" flex flex-col p-5"> 

      <div class="flex flex-col mb-5">
        <span class="mb-3"> استاد </span>
        <UInputMenu v-model="selected" :options="people" />
      </div>
      
      <div class="flex flex-col mb-5">
        <span class="mb-3">عنوان</span>
        <UInput color="primary" variant="outline" placeholder="عنوان وظیفه را مشخص کنید" />
      </div>

      <div class="flex flex-col mb-5">
        <span class="mb-3">توضیحات</span>
        <UTextarea color="primary" variant="outline" placeholder="توضیحات لازم را وارد کنید" />
      </div>

      <div class="flex flex-col mb-5">
        <span class="mb-3">تاریخ انقضا</span>
        <input type="date"/>
      </div>


      <div class="w-full flex mt-5 justify-center items-center">
        <UButton label="ذخیره" color="primary" class="px-5 mx-2" />
        <UButton to="/" label="بازگشت" color="rose" class="px-5 mx-2" />
      </div>
  
    </div>
  </div>


</template>

<script lang="ts" setup>

const people = ['مهدی کلانتری','احمد شیرانی','ستایش جعفری','محمد رضا زرگرزاده','سید علی آزمایش','احمد قنواتی']

const selected = ref()

const id = ref('10')
const title = ref('عنوان وظیفه')
const description = ref("")

</script>

<style>

</style>