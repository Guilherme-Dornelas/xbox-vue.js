<template>    
       <HeaderComponente />   
       <BannerComponente />   
       <ControleComponente />   
       <CarrousselComponente />  
        <FaqComponente /> 
        <FooterComponente /> 
</template>

<script>
import BannerComponente from '@/components/bannerComponente.vue';
import CarrousselComponente from '@/components/carrousselComponente.vue';
import ControleComponente from '@/components/controleComponente.vue';
import FaqComponente from '@/components/faqComponente.vue';
import FooterComponente from '@/components/footerComponente.vue';
import HeaderComponente from '@/components/headerComponente.vue';


export default {
  name: 'homePage',
    components:{
        HeaderComponente,
        BannerComponente,
        ControleComponente,
        CarrousselComponente,
        FaqComponente,
        FooterComponente
    }

  } 


</script>