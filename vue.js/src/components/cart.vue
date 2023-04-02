<template>
    <div>
<h1>Cart</h1>
<div class="alblums">
  <div v-for="(product, index) in cart" :key="index">
 <h3>{{ product.name }}</h3>
    <img :src="product.img" />
  <div>{{ product.artist }}</div>
  <div>{{ product.price }}</div>
  <button v-on:click="removeitem(products)">Remove From Your Cart</button>
  </div> 
</div>
</div>
</template>

<script>
export default {
    props: ["cart"],
    methods: {
        removeitem(product) {
            this.$emit("removeitem", product);
        }
    }
};
</script>



<style>
</style>