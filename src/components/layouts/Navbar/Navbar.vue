<script setup>
import { ref, watch } from "vue";
import {useI18n} from "vue-i18n";
const i18n = useI18n();

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

<ul class="nav__list">
    <li class="nav__link"><a  class="nav-link-list" href="">{{$t('Asosiy')}}</a></li>
    <li class="nav__link"><a  class="nav-link-list" href="#about">{{$t('Biz haqimizda')}}</a></li>
    <li class="nav__link"><a  class="nav-link-list" href="#uslug">{{ $t('Xizmatlar') }}</a></li>
    <li class="nav__link"><a  class="nav-link-list" href="#faq">{{$t('Faq')}}</a></li>
</ul>
<select  @input="lenginputed($event.target.value)">
  <option value="uz">O'zbekcha</option>
  <option value="ru">Ruscha</option>
</select>

<a href="#contact" class="nav__main-link">{{$t('Kirish')}}</a>
</div>
</div>
  </nav>
</template>



<style>

</style>