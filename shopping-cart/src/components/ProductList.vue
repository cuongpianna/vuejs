<template id="">
  <div class="">
    <h1>Product list</h1>
    <ul>
      <li v-for='product in products'>{{product.title}} - {{product.price}}</li>
    </ul>
  </div>
</template>

<script type="text/javascript">
  import shop from '@/api/shop'
  export default {
    data(){
      return {
        products : []
      }
    },

    created(){
      shop.getProducts(products => {
        this.products = products
      })
    }
  }
</script>

<style scoped>

</style>
