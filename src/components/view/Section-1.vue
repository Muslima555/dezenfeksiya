<script setup>

</script>


<template>
<div class="container">

    <div class="section1__content" id="about">
        <h1 class="section1__content-title">{{$t('Avfzalliklarimiz')}}</h1>

      <div class="section1__content-cards">


        <div class="section1__content-card">
            <img src="@/assets/img/Mask group (1).png" alt="">
            <h4 class="section1__card-title">{{$t('Tezda xizmat ko’rsatish')}}</h4>
            <p class="section1__card-text">{{ $t("ARIZALAR KUNIGA 24 SOAT QABUL QILINADI. AGAR MUAMMO SHOSHILINCH BO'LSA, BIZ DARHOL KELISHIMIZ MUMKIN. BIROQ, SIFAT JUDA YAXSHI.") }}</p>
        </div>

        <div class="section1__content-card">
            <img src="@/assets/img/Mask group.png" alt="">
            <h4 class="section1__card-title">{{$t('Bizning Tajribali Mutaxassislarimiz')}}</h4>
            <p class="section1__card-text">{{ $t("BIZNING XODIMLARIMIZ HAMMA NARSANI O'Z ICHIGA OLADI: BUXGALTERIYA HISOBI, BINOLARNI TAYYORLASH, QAYTA ISHLASH, YAKUNIY TOZALASH, SHAMOLLATISH VA NAZORAT TEKSHIRUVLARI") }}</p>
        </div>

        <div class="section1__content-card">
            <img src="@/assets/img/Mask group (2).png" alt="">
            <h4 class="section1__card-title">{{$t("Sizga Qulay Bo'lganda")}}</h4>
            <p class="section1__card-text">{{ $t("SIZGA MOS VA QULAY VAQTNI TANLANG VA BIZ BILAN BOG'LANING. BIZ SIZGA KAFOLATLANGAN VA SAMARALI NATIJA BERAMIZ") }}</p>
        </div>



      </div>


    </div>

<div class="section1__picture">
    <h1 class="section1__picture-title">{{$t('Klapa va zararli hashorot endi yo’q deb hisoblang !!')}}</h1>
    <p class="section1__picture-text">{{ $t('Bizning ko’p yillardan beri o’z faoliyatini olib kelayotgan kompaniyamiz Mijozlarimiz bizdan mamnun') }}</p>
    <a href="#contact" class="left__link">{{ $t('Bog’lanish') }}</a>
</div>

</div>
</template>



<style>

</style>