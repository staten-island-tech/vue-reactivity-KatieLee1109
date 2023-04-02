<template>
  <div>
  <h1>Yayaya</h1>
  <div v-for="product in products" :key="product.name">{{ product.name }}
  <img :src="product.img" />
  </div>
  </div>
</template>\

<script>
export default {
  name: "App",
  data: () => {
    return{
      products:[
        {
          name: "Twicetagram",
          artist: "Twice",
          price: "15.50",
          img: "https://upload.wikimedia.org/wikipedia/en/e/eb/Twicetagram_album_cover.png"
        },
        {
          name: "Merry and Happy",
          artist: "Twice",
          price: "16.00",
          img: "data:image/jpeg;base64,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"
        },
        {
          name: "Map of the Soul: 7",
          artist: "BTS",
          price: "18.00",
          img: "https://upload.wikimedia.org/wikipedia/en/2/21/BTS_-_Map_of_the_Soul_7.png",
        },
        {
          name: "Love Yourself: Tear",
          artist: "BTS",
          price: "19.00",
          img: "https://upload.wikimedia.org/wikipedia/en/8/88/Love_Yourself_Tear_Cover.jpeg",
        },
        {
          name: "The Most Beautiful Moment in Life: Young Forever",
          artist: "BTS",
          price: "19.00",
          img: "https://upload.wikimedia.org/wikipedia/en/b/b4/The_Most_Beautiful_Moment_In_Life%2C_Young_Forever.jpeg",
        },
        {
          name: "Love Yourself: Answer",
          artist: "BTS",
          price: "19.00",
          img: "https://upload.wikimedia.org/wikipedia/en/e/e2/BTS%2C_Love_Yourself_Answer%2C_album_cover.jpg",
        },

      ]
    }
  }
};
components: {}
</script>

<style>
</style>