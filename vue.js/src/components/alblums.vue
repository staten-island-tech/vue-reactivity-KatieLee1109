<template>
    <div>
  <h1>Alblums</h1>
  <div class="alblums">
  <div v-for="(product, index) in products" :key="index">
    <h3>{{ product.name }}</h3>
  <img :src="product.img" />
  <div>{{ product.artist }}</div>
  <div>{{ product.price }}</div>
  <button v-on:click="additem(product)">Add to Your Cart</button>
  </div> 
  </div>
</div>
</template>

<script>
export default {
    data: () => {
    return{
        products: [
        {
          name: "Twicetagram",
          artist: "Twice",
          price: "$15.50",
          img: "https://upload.wikimedia.org/wikipedia/en/e/eb/Twicetagram_album_cover.png"
        },
        {
          name: "Merry and Happy",
          artist: "Twice",
          price: "$16.00",
          img: "https://upload.wikimedia.org/wikipedia/en/b/b8/Twice-Merry_%26_Happy_%28album_cover%29.jpg"
        },
        {
          name: "Map of the Soul: 7",
          artist: "BTS",
          price: "$18.00",
          img: "https://upload.wikimedia.org/wikipedia/en/2/21/BTS_-_Map_of_the_Soul_7.png",
        },
        {
          name: "Love Yourself: Tear",
          artist: "BTS",
          price: "$19.00",
          img: "https://upload.wikimedia.org/wikipedia/en/8/88/Love_Yourself_Tear_Cover.jpeg",
        },
        {
          name: "The Most Beautiful Moment in Life: Young Forever",
          artist: "BTS",
          price: "$19.00",
          img: "https://upload.wikimedia.org/wikipedia/en/b/b4/The_Most_Beautiful_Moment_In_Life%2C_Young_Forever.jpeg",
        },
        {
          name: "Love Yourself: Answer",
          artist: "BTS",
          price: "$19.00",
          img: "https://upload.wikimedia.org/wikipedia/en/e/e2/BTS%2C_Love_Yourself_Answer%2C_album_cover.jpg",
        },
        {
          name: "Go Live",
          artist: "Stray Kids",
          price: "$20.00",
          img: "https://upload.wikimedia.org/wikipedia/en/2/2b/Stray_Kids_-_Go_Live.png"
        },
        {
          name: "Into The New World",
          artist: "Girls' Generation",
          price: "$25.00",
          img: "https://upload.wikimedia.org/wikipedia/en/1/12/Intothenewworldtour.jpg"
        },
        {
        name: "The Sound",
        artist: "Stray Kids",
        price: "$21.00",
        img: "https://upload.wikimedia.org/wikipedia/en/8/8f/Stray_Kids_-_The_Sound.png"
        },
        {
          name: "Oddinary",
          artist: "Stray Kids",
          price: "$30.00",
          img: "https://upload.wikimedia.org/wikipedia/en/4/45/Stray_Kids_-_Oddinary.jpeg"
        }
      ]
    };
},
methods: {
    additem(product){
        this.$emit("additem", product);
    }
}
};
</script>
<style>
</style>