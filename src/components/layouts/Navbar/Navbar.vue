<script setup>
import { ref, watch } from "vue";
import {useI18n} from "vue-i18n";
const i18n = useI18n();
const burger = ref(false)
const lenginput = ref("EN");
function lenginputed (item){
    lenginput.value = item
}


watch( lenginput,()=>{
   if( lenginput.value == "uz"){
    i18n.locale.value= 'uz'
   } else if( lenginput.value == "ru"){
     i18n.locale.value = 'ru' 
   }
})

</script>


<template>
 <nav class="nav">
<div class="container">
<div class="nav__content">
    <div class="nav__logo">
    <img src="@/assets/img/Union.png" alt="">
    <h2 class="nav__logo-title">{{ $t('Dizenfeksiya') }}</h2>
    </div>


 


<!-- ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~burger navigation~~~~~~~~~~~~~~~~~~~~~~~~~ -->
<div class="nav__list-burger-navigation"
 :class="{'activeburger': burger }"
>
  <button class="btn__list-burger-exit" @click="burger = false">X</button>
  <ul class="nav__list-burger">
    <li ><a class="burger__list-link" href="">{{$t('Asosiy')}}</a></li>
    <li ><a class="burger__list-link" href="#about">{{$t('Biz haqimizda')}}</a></li>
    <li ><a class="burger__list-link" href="#uslug">{{ $t('Xizmatlar') }}</a></li>
    <li ><a class="burger__list-link" href="#faq">{{$t('Faq')}}</a></li>
</ul>

 

</div>


<ul class="nav__list">
    <li class="nav__link"><a class="nav-link-list" href="">{{$t('Asosiy')}}</a></li>
    <li class="nav__link"><a class="nav-link-list" href="#about">{{$t('Biz haqimizda')}}</a></li>
    <li class="nav__link"><a class="nav-link-list" href="#uslug">{{ $t('Xizmatlar') }}</a></li>
    <li class="nav__link"><a class="nav-link-list" href="#faq">{{$t('Faq')}}</a></li>
</ul>


<select class="lenguage-con"  @input="lenginputed($event.target.value)">
  <option value="uz">O'zbekcha</option>
  <option value="ru">Ruscha</option>
</select>

<!-- ~~~~~~~~~~~~~~~~~~~~burger navigation btn~~~~~~~~~~~~~~ -->
<button class="btn__active-burger" @click="burger = true"><svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 448 512"><path d="M0 96C0 78.3 14.3 64 32 64l384 0c17.7 0 32 14.3 32 32s-14.3 32-32 32L32 128C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32l384 0c17.7 0 32 14.3 32 32s-14.3 32-32 32L32 288c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32L32 448c-17.7 0-32-14.3-32-32s14.3-32 32-32l384 0c17.7 0 32 14.3 32 32z"/></svg></button>


<a href="#contact" class="nav__main-link">{{$t("Bog'lanish")}}</a>
</div>
</div>
  </nav>
</template>



<style >

</style>