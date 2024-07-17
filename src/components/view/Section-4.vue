<script setup>
import { ref } from 'vue';
import { toast } from 'vue3-toastify';
import 'vue3-toastify/dist/index.css';
const token = import.meta.env.VITE_TG_TOKEN
const chatId = import.meta.env.VITE_TG_CHATID


const text= ref("")
const number =ref("")
const chek =ref("")
const notify = ()=>{
  toast("Successfully sent!",{
    autoClose:1000,
  });
}

function submit () {
 const fullMessage = `name:${text.value}, number: ${number.value}`
 fetch(`https://api.telegram.org/bot${token}/sendMessage?chat_id=${chatId}&text=${fullMessage}`);
 text.value= "";
 number.value =""
 notify()
}
</script>


<template>
<div class="container">
<div class="section4__content">
<div class="section4__left">
    <h1 class="section4__title">Malumotingizni qoldiring</h1>
    <form action="" @submit.prevent="submit" >
    <input required type="text" v-model="text" placeholder="Ism" class="section4__input">
    <input required type="number" v-model="number" placeholder="+998 |" class="section4__input">
    <div class="section4__checkbox-main">
    <input v-model="chek" type="checkbox" class="section4__checkbox">
    <label class="section4__subtitle">Maxfiylik siyosati</label>
   </div>
    <button type="submit"   class="section4__link">Yozilish</button>
</form>
</div>
<div class="section4__right">
    <h4 class="section4__right-title">Bizga ko'p yillardan beri  kompaniyamizga ishonch bildirganlar talaygina</h4>
    <img src="@/assets/img/person.png" alt="" class="section4__img">
</div>
</div>
</div>


</template>



<style>

</style>