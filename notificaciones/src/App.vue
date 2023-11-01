<script setup>
// import { onBeforeMount, ref } from 'vue'

import { ref } from 'vue';

// //import HelloWorld from './components/HelloWorld.vue'
// //import TheWelcome from './components/TheWelcome.vue'


// onBeforeMount(() => {
//   setTimeout(() => {
//     fetch('https://jsonplaceholder.typicode.com/posts/1')
//       .then((response) => response.json())
//       .then((json) => {
//         //res = JSON.parse(json)
//         msg.value = json.title
//         loading.value = false
//       })
//   }, 3000)

//   //msg.value = localStorage.getItem('msg')
// })

// let msg = ref('coco77')
// let loading = ref(true)



// function cambia() {
//   msg.value = 'hola'
//   console.log(msg.value)
// }





let qty = ref(2)

function addValue(n){
  qty.value+n;
  console.log(qty.value);
}

function subtractValue(){

  qty.value--;
  console.log(qty.value);
}



</script>

<template>
  <div class="wrapper">
    <div class="profile">  
      <div class="balloon" v-if="qty > 0">{{ qty }}</div>
    </div>

    <div class="button-wrapper">
      <div class="button" @click="subtractValue">-</div>
      <div class="button" @click="addValue(77)">+</div>
    </div>
    <div v-if="qty">Me escribieron 😊</div>
    <div v-else>Nadie me escribe ❤</div>
  </div>

</template>

<style scoped>

.button{
  display: inline-block;
  width: 32px;
  background-color: antiquewhite;
  padding: 4px 0px;
  border-radius: 4px;
  margin: 0 10px;
 
}

.button:hover{
  
  cursor: pointer;
  background-color: rgb(201, 56, 201);
  transition: 0.7s;
}

.balloon:hover{
  cursor: pointer;
  
}

.button-wrapper{
  text-align: center;
  margin-top: 16px;
  margin-bottom: 16px;
}
.balloon{
  top: 0;
  right: 0;
  background-color: rgba(177, 17, 177, 0.862);
  width: 32px;
  height: 32px;
  border-radius: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  position: absolute;
}
.profile {
  position: relative;
  background-image: url(https://media.licdn.com/dms/image/D4E03AQE72ePewxr9Rg/profile-displayphoto-shrink_800_800/0/1682260228509?e=2147483647&v=beta&t=rNudKzS24q3kit-1N8zi-XW7PeIdZT48GmPOUa1JpuQ);
  background-size:cover ;
  background-color: blueviolet;
  width: 120px;
  height: 120px;
  margin: 0 auto;
  border-radius: 100%;
}
.wrapper {
  overflow: hidden;
  padding-top: 18px;
  background-color: rgba(158, 43, 158, 0.726);
  width: 60%;
  border-radius: 12px;
  margin: 0 auto;
  
}
</style>
