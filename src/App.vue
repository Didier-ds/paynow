<template>
  <div class="wrapper sm:grid flex flex-col justify-center grid-cols-2">
      <div class="py-4">
        <div class="mx-auto w-10/12">
          <Logo />
        <GoBack />
        <Product @toggleSlide = "toggleSlide"/>
        <div class="hidden sm:block">
          <Footer />
        </div>
        
        </div>
      </div>
      <div class="slider bg-white z-10 py-4">
        <FormSlider />
        <div class="block w-10/12 mx-auto py-4 sm:hidden">
          <Footer />
        </div>
      </div>
      
  </div>
</template>

<script setup>
// import HelloWorld from './components/HelloWorld.vue'
import GoBack from '@/components/Goback.vue'
import Logo from '@/components/Logo.vue'
import Product from '@/components/Product.vue'
import FormSlider from '@/components/FormSlider.vue'
import Footer from '@/components/Footer.vue'

</script>

<style lang="scss">
@import "./assets/styles/main.scss";
@media (min-width: 1024px) {
  .wrapper {
  max-width: 90%;
}

}

.wrapper {
  margin: 0 auto;
  min-height: 100vh;
  
}

.slider {

  position: relative;
  // padding:1em 0;
}
.slider::before {
  content: "";
  position: absolute;
  height: 100%;
  width: 1px;
  top:0;
  left:0;
  // background: #3c42577e;
  box-shadow: -2px 0px 10px 0px rgba(0, 0, 0, 0.28);
}

</style>
