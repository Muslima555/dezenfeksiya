<script setup>
  import { ref, watch } from 'vue';
  
  
  const activeKey = ref(['']);
  
  watch(activeKey, val => {
    console.log(val);
  });
</script>


<template>

 <div class="container faqs">
    <h1 class="logo-faq">FAQ</h1>
  <a-collapse v-model:activeKey="activeKey">
      <a-collapse-panel key="1" class="text-1-collapse" header="Zararkunandalarni yo'q qilish qanday amalga oshiriladi?">
        <p>Mahsus asbob-uskunalar yordamida insektitsidlar aerozolli tumanga aylanadi va devor qog'ozi, devorlar va taxta plitalari orasidagi eng kichik bo'shliqlarga, ko'zga ko'rinmas hashorotlar uchun potentsial 'yashirish joylari' ga kiradi.
        </p>
      </a-collapse-panel>
      <a-collapse-panel key="2" class="text-1-collapse" header="Siz foydalanadigan dorilar havflimi?">
        <p>Preparatlar olamlar, uy hayvonlari va o'simliklar uchun havfli emas. Ammo davolanishdan keyin honani 40 daqiqa davomida ventilyatsiya qilish kerak.
        </p>
      </a-collapse-panel>
      <a-collapse-panel key="3" class="text-1-collapse" header="Menga uyimni davolanishga tayyorlashning qandaydir usuli kerakmi?">
        <p>Asosan, idish-tovoq va shahsiy gigiena vositalarini izolyatsiya qilishingiz kerak. Davolash paytida uy hayvonlari ham izolyatsiya qilinish kerak. Mebel yoki maishiy tehnikani ko'chirishga hojat yo'q.
        </p>
      </a-collapse-panel>
    </a-collapse>
 </div>


</template>



<style>
.logo-faq{
  font-size: 42px;
  font-weight: 700;
}
span.ant-collapse-header-text{
  font-size: 32px;
}
/* div.ant-collapse-expand-icon.css-dev-only-do-not-override-19iuou{

} */
div.ant-collapse-header{
  display: flex;
  align-items: center !important;
  max-width: 1000px;
  width: 100%;
  background: transparent !important;
}
.ant-collapse{
  background: transparent !important;
  border: none;
}
div.ant-collapse-content-box{
  max-width: 1000px;
  width: 100%;
  font-size: 22px;
}
.faqs{
  display: flex;
   justify-content: space-between;
   border-top:1px solid rgba(0, 0, 0,0.2);
   padding:30px 5px;
}
@media (max-width: 768px) {
  .faqs {
    flex-direction: column;
    align-items: stretch; /* по умолчанию */
  }
  .logo-faq{
    text-align: center;
  }
  div.ant-collapse-content-box{
  max-width: 1000px;
  width: 100%;
  font-size: 16px;
 }
 span.ant-collapse-header-text{
  font-size: 22px;
}
 .logo-faq{
  font-size: 32px;
  font-weight: 700;
}

}
svg{
  width: 40px;
  height: 40px;
  border: 1px solid black;
  padding: 10px;
  border-radius: 50%;
}
</style>