<script setup>
import navbar from '@/components/layouts/Navbar/Navbar.vue'
</script>



<template>
   <header>
    <navbar/>
<div class="container">
    <div class="header__content">
        <div class="header__content-left">
            <h1 class="header__content-left-title">{{ $t('Dizenfeksiya xizmati') }}</h1>
            <p class="header__content-left-text">{{ $t('Bizning ko’p yillardan beri o’z faoliyatini olib kelayotgan kompaniyamiz Mijozlarimiz bizdan mamnun') }}</p>
            <div class="left__box">
            <a href="" class="left__link">{{ $t('Bog’lanish') }}</a>
             <img class="left__img" src="@/assets/img/Vector 5.png" alt="">
            </div>
        </div>
        <div class="header__content-right">
        <img class="header__content-right-img" src="@/assets/img/WnYJyJjWq3U 1.png" alt="">
        </div>
    </div>
</div>

   </header>
</template>



<style>

</style>