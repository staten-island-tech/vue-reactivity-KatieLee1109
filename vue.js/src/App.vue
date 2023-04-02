<template>
  <div>
  <header>
    <button v-on:click="navigateTo('product')">Products</button>
    {{ cart.length }} in cart
  <button v-on:click= "navigateTo('cart')">View Cart</button>
  </header>


  <div v-if="page === 'cart'">
<cart v-on:removeitem="removeitem" :cart="cart" />
</div>

<div v-if="page === 'product'">
<alblums v-on:additem="additem" />
</div>
</div>
</template>


<script>
import alblums from './components/alblums.vue';
import cart from './components/cart.vue';

export default {
  name: "App",
  data: () => {
    return {
      page: "products",
      cart: [],
    };
  },
  methods: {
    additem(product){
      this.cart.push(product);
    },
    removeitem(product){
      this.cart.splice(this.cart.indexOf(product)
      );
    },
    navigateTo(page){
      this.page = page;
    }
    },
  components: {alblums, cart}
};


</script>

<style>
</style>