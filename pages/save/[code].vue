<template>
  <div class="flex flex-col" style="direction: rtl;">
    <Header title="ثبت اطلاعات انجام پروژه" />
    <div class=" flex flex-col p-5"> 


      <div class="w-full text-xs my-5 text-center">
        <span> شما در حال ثبت اطلاعات برای : </span>
        <span class="font-bold mr-2"> {{ title }} </span>
      </div>
      
      <div class="flex flex-col mb-5">
        <span class="mb-3"> کارآموز </span>
        <UInputMenu v-model="selected" :options="people" />
      </div>
      
      <div class="flex flex-col">
        <span class="mb-3"> لینک</span>
        <UInput color="primary" variant="outline" placeholder="لینک گیت هاب" />
      </div>

      <div class="w-full flex mt-5 justify-center items-center">
        <UButton label="ذخیره" color="primary" class="px-5 mx-2" />
        <UButton to="/" label="بازگشت" color="rose" class="px-5 mx-2" />
      </div>
  
    </div>
  </div>


</template>

<script lang="ts" setup>

const people = ['آرش شریفی', 'کیمیا' ,'زهرا دهقانی','محمد شفیع زاده','محمدهادی معصومی','محمد جواد عباسپور']

const selected = ref()

const id = ref('10')
const title = ref('عنوان وظیفه')
const description = ref("")

</script>

<style>

</style>