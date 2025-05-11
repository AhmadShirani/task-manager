<template>
  <div class="flex flex-col" style="direction: rtl;">
    <Header title="مشخصات وظیفه" />
    <div class=" flex flex-col p-5"> 
      <span class="w-full my-5 text-center text-lg font-bold"> {{ title }} </span>

      <div>
        <div class='w-full p-2' style='direction: rtl;'>
          <span> عنوان وظیفه </span>
          <p> تکالیف روز شنبه: </p>
          <p> 🔺مشاهده ویدیو های شماره ۸ تا ۱۰ (حتما نکات مهم یادداشت برداری شود.)   </p>
          <p> 🔺افزودن اکستنشن یا افزونه های زیر در vscode </p>
          <p> Live server  </p>
          <p> Auto rename tag  </p>
          <p> Auto complete tag   </p>
          <p> Auto close tag </p>
          <p>🔺ساخت اکانت و ثبت نام در Git Hub </p>
          <p>🔺ساخت یک فایل html </p>
          <p> رنگ پس زمینه: beige </p>
          <p> افزودن تصویر لوگو به بالای صفحه  </p>
          <p> ایجاد یک فرم شامل ۳ input و label </p>
          <p> نام </p>
          <p> ایمیل </p>
          <p> شماره تماس </p>
          <p> و افزودن یک دکمه با نام تایید و رنگ سبز به انتهای کار </p>
          <p>  </p>
          <p> با تشکر از شما </p>
        </div>
      </div>

      <div class="w-full flex mt-3">
        <UButton :to="`/save/${id}`" label="انجام دادم" class="mx-auto px-5" />
      </div>
      
    </div>
  </div>


</template>

<script lang="ts" setup>

const id = ref('10')
const title = ref('عنوان وظیفه')
const description = ref("")

</script>

<style>

</style>