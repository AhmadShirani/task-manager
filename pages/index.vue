<script setup lang="ts">
    const list = ref<any[]>([])
    const dummy = [
        {id : 1,title:'تمرین شماره 1' , expireDate : '1404-02-30' , leader:'علی'},
        {id : 2,title:'تمرین شماره 2' , expireDate : '1404-02-20' , leader:'رضا'},
        {id : 3,title:'تمرین شماره 3' , expireDate : '1404-03-10' , leader:'محسن'},
        {id : 4,title:'تمرین شماره 4' , expireDate : '1404-03-12' , leader:'علی'},
        {id : 5,title:'تمرین شماره 5' , expireDate : '1404-04-24' , leader:'مهدی'},
    ]
    onMounted(async () => { 
      list.value = dummy;      
    });
</script>

<template>
    <div class="p-3 flex flex-col">
        <span class="w-full text-center font-bold mt-3"> وظایف کارآموزان تجارت الکترونیک بیست آفاق ایرانیان </span>

        <div class="grid grid-cols-1 gap-3 mt-5">
    
    <Item 
    v-for="(option,i) in list" 
    :key="`item_${i}`" 
    :id="option.id" 
    :title="option.title" 
    :expireDate="option.expireDate" 
    :leader="option.leader"/>
</div>

<UButton to="/joketeller" label="JokeTeller" color="rose" class="px-5 mt-4 mx-2" />
    </div>
</template>

<style>
    
</style>
