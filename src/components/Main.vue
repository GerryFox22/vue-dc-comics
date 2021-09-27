<template>
  <main>
        <div class="jumbo">
            <img src="../assets/jumbotron.jpg" alt="">
            <div class="jumbo-elements">
                <h2>CURRENT SERIES</h2>

                <div class="comics-cards-container">
                   <Card v-for="(card,index) in dcComics" :key="index" :image="card.thumb" :price="card.price" :series="card.series" :type="card-type" />
                </div>

                <div class="load-button-container">
                    <button class="load-button">LOAD MORE</button>
                </div>
                    
            </div>
        </div>
          
        <div class="bg-info-container">
            <div class="info-container">
                <div v-for="(info, index) in informations" :key="index" class="single-info">
                    <img :src="info.src" :alt="info.alt">
                    <p>{{ info.text }}</p>
                </div>
                
            </div>
        </div>
      
  </main>
</template>

<script>

import dcComics from "../data/dc-comics.js"
import Card from "../components/card.vue"

export default {
    name: "Main",

    components: {
    Card,
  },

    data: function() {
        return {

            informations : [
                {
                    text : "DIGITAL COMICS",
                    src : "./img/buy-comics-digital-comics.png",
                    alt : "DIGITAL COMICS IMG"

                },
                {
                    text : "DC MERCHANDISE",
                    src : "./img/buy-comics-merchandise.png",
                    alt : "DC MERCHANDISE IMG"

                },
                {
                    text : "SUBSCRIPTION",
                    src : "./img/buy-comics-subscriptions.png",
                    alt : "SUBSCRIPTION IMG"

                },
                {
                    text : "COMIC SHOP LOCATOR",
                    src : "./img/buy-comics-shop-locator.png",
                    alt : "COMIC SHOP LOCATOR IMG"

                },
                {
                    text : "DC POWER VISA",
                    src : "./img/buy-dc-power-visa.svg",
                    alt : "DC POWER VISA IMG"
                },
            ],
            dcComics,
        }
    },
    methods: {

    },
}
</script>

<style lang="scss" scoped>
@import "../style/variables.scss";

main {
    background-color: black;
}

.jumbo {
    background-color: black;
    img {
        width: 100%;
        height: 350px;
        object-fit: cover;
        object-position: top;
    }
}


.jumbo-elements {
    width: 80%;
    margin: 0 auto;
    margin-bottom: 20px;
    h2 {
        color: $whiteText ;
        margin: 0;
        background-color: #0282F9;
        width: 17%;
        padding: 20px;
        font-size: 1.3rem;
    }
    button {
        background-color: #0282F9;
        color: $whiteText ;
        width: 15%;
        padding: 5px 0;
        cursor: pointer;
        
    }
}

.load-button-container {
    text-align: center;
}

.comics-cards-container{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin: 20px 0;
}

.main-container,
.info-container {
    width: 80%;
    margin: 0 auto;
}

.info-container {
    display: flex;
    justify-content: space-around;
}

.bg-info-container {
    background-color: $dc-blue;
}

.single-info {
    display: flex;
    align-items: center;
    padding: 20px 0;
 
}

.single-info p {
    font-size: .6rem;
    padding-left: 15px;
}

h4 {
   padding: 40px 0;
}

img {
    width: 30px;
}

h4,
p {
    color: $whiteText;
    margin: 0;
}

</style>