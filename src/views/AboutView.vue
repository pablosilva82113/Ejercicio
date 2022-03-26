<template>
  <div class="about">
    <FormuPedido></FormuPedido>
    <AlmacenIn></AlmacenIn>
    <AlmacenAd></AlmacenAd>
  </div>
</template>
<script>
import FormuPedido from '../components/FormuPedido.vue'
import AlmacenIn from '../components/AlmacenIn.vue'
import AlmacenAd from '../components/AlmacenAd.vue'
  export default {

    name: 'AboutView',
    components: {
      FormuPedido,
      AlmacenIn,
      AlmacenAd
    }

  }
</script>
