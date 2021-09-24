<template>
  <main>
        <div class="content-container">
            <div class="content">
              <h4>--- Content goes here ---</h4>
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
export default {
    name: "Main",

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


.content-container {
    width: 80%;
    margin: 0 auto;
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