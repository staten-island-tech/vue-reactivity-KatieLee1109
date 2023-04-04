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
          name: "Rare",
          artist: "Selena Gomez",
          price: "$25.50",
          img: "https://upload.wikimedia.org/wikipedia/en/d/d1/Selena_Gomez_-_Rare.png"
        },
        {
          name: "Sweetener",
          artist: "Ariana Grande",
          price: "$16.00",
          img: "https://upload.wikimedia.org/wikipedia/en/7/7a/Sweetener_album_cover.png"
        },
        {
          name: "Thank U, Next",
          artist: "Ariana Grande",
          price: "$18.00",
          img: "https://upload.wikimedia.org/wikipedia/en/b/b2/Ariana_Grande_Thank_U_Next.png",
        },
        {
          name: "Divide",
          artist: "Ed Sheeran",
          price: "$19.00",
          img: "https://upload.wikimedia.org/wikipedia/en/4/45/Divide_cover.png",
        },
        {
          name: "=",
          artist: "Ed Sheeran",
          price: "$19.00",
          img: "https://upload.wikimedia.org/wikipedia/en/c/cd/Ed_Sheeran_-_Equals.png",
        },
        {
          name: "Doo-Wops & Hooligans",
          artist: "Bruno Mars",
          price: "$19.00",
          img: "https://upload.wikimedia.org/wikipedia/en/e/eb/Bruno_Mars_-_Doo-Wops_%26_Hooligans.png",
        },
        {
          name: "Unorthodox Jukebox",
          artist: "Bruno Mars",
          price: "$20.00",
          img: "https://upload.wikimedia.org/wikipedia/en/7/77/BrunoMarsUJAlbumCover.png"
        },
        {
          name: "Joanne",
          artist: "Lady Gaga",
          price: "$25.00",
          img: "https://upload.wikimedia.org/wikipedia/en/f/fd/Lady_Gaga_-_Joanne_%28Official_Album_Cover%29.png"
        },
        {
        name: "A Star Is Born",
        artist: "Lady Gaga",
        price: "$21.00",
        img: "https://upload.wikimedia.org/wikipedia/en/e/e0/A_Star_Is_Born_%282018_soundtrack%29.png"
        },
        {
          name: "Harry's House",
          artist: "Harry Styles",
          price: "$30.00",
          img: "https://upload.wikimedia.org/wikipedia/en/d/d5/Harry_Styles_-_Harry%27s_House.png"
        },
        {
          name: "Midnights",
          artist: "Taylor Swift",
          price: "$30.00",
          img: "https://upload.wikimedia.org/wikipedia/en/9/9f/Midnights_-_Taylor_Swift.png"
        },
        {
          name: "Lover",
          artist: "Taylor Swift",
          price: "$35.00",
          img: "https://upload.wikimedia.org/wikipedia/en/c/cd/Taylor_Swift_-_Lover.png"
        },
        {
          name: "Reputation",
          artist: "Taylor Swift",
          price: "$30.00",
          img: "https://upload.wikimedia.org/wikipedia/en/f/f2/Taylor_Swift_-_Reputation.png"
        },
        {
          name: "Fearless",
          artist: "Taylor Swift",
          price: "$28.00",
          img: "https://upload.wikimedia.org/wikipedia/en/8/86/Taylor_Swift_-_Fearless.png"
        },
        {
          name: "Folklore",
          artist: "Taylor Swift",
          price: "$30.00",
          img: "https://upload.wikimedia.org/wikipedia/en/f/f8/Taylor_Swift_-_Folklore.png"
        },
        {
          name: "Red- Taylor's Version",
          artist: "Taylor Swift",
          price: "$32.00",
          img: "https://upload.wikimedia.org/wikipedia/en/4/47/Taylor_Swift_-_Red_%28Taylor%27s_Version%29.png"
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