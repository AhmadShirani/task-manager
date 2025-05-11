<template>
  <div class="flex flex-col items-center justify-center p-10">


    <div class="my-10" style="direction: ltr;">
      <p class="mb-2"> {{ category }} </p>
    <p class=""> {{ joke }} </p>
    </div>

    <div class="flex justify-between">
      <UButton label="دریافت جک جدید" color="primary" class="px-5 mx-2" @click="getNewJoke" />
    <UButton label="دریافت جک 2" color="primary" class="px-5 mx-2" @click="getNewJoke2" />
    </div>

    <UButton to="/" label="بازگشت" color="rose" class="px-5 mt-4 mx-2" />
    
  </div>
</template>

<script lang="ts" setup>
//#region Instance
import axios from 'axios';
//#endregion 

//#region Variables
const joke = ref<string>('')
  const category = ref<string>('')
//#endregion 

//#region ASYNC / AWAIT
  const getNewJoke2 = async () => {
  try {
    const response = await axios.get('https://sv443.net/jokeapi/v2/joke/Any');
    console.log(response);
    joke.value = response.data.setup
    category.value = response.data.category
  } catch (error) {
    console.error(error);
  }
}
//#endregion 

//#region PROMISE
const getNewJoke = () => {

  axios.get('https://sv443.net/jokeapi/v2/joke/Any')
  .then((response) => {
    joke.value = response.data.setup
    category.value = response.data.category
  })
  .catch((error)=> {
    // handle error
    console.log(error);
  })
  .finally(()=> {
    // always executed
  });

}
//#endregion 

onMounted(async () => { 
  getNewJoke2() 
    });

</script>

<style>

</style>