<template>
  <header id="header">
      <img :src="'./img/dc-logo.png'" alt="DC Logo">
      <nav>
          <ul>
              <li v-for="(link, index) in links" :key="index" :class="{ active : link.current }">
                  <a :class="{ active : link.current }" :href=" link.url ">{{ link.text }}</a>
              </li>
          </ul>
      </nav>
  </header>
</template>

<script>
export default {
    name: "Header",

    data: function() {
        return {

            links : [
                {
                    text : "CHARACTERS",
                    url : "#CHARACTERS",
                    current : false,
                },
                {
                    text : "COMICS",
                    url : "#COMICS",
                    current : true,
                },
                {
                    text : "MOVIES",
                    url : "#MOVIES",
                    current : false,
                },
                {
                    text : "TV",
                    url : "#TV",
                    current : false,
                },
                {
                    text : "GAMES",
                    url : "#GAMES",
                    current : false,
                },
                {
                    text : "COLLECTIBLES",
                    url : "#COLLECTIBLES",
                    current : false,
                },
                {
                    text : "VIDEOS",
                    url : "#VIDEOS",
                    current : false,
                },
                {
                    text : "FANS",
                    url : "#FANS",
                    current : false,
                },
                {
                    text : "NEWS",
                    url : "#NEWS",
                    current : false,
                },
                {
                    text : "SHOP",
                    url : "#SHOP",
                    current : false,
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

header {
    display: flex;
    justify-content: space-between;
    padding: 25px 0;
    width: 80%;
    margin: 0 auto;
}

img{
    width:90px;
}

ul {
    display: flex;
    padding: 0;
    margin: 0;
    align-items: center;
    height: 100%;
}

ul li {
    padding: 20px;
    list-style: none;
         &.active {
            color: $dc-blue;
            border-bottom: 5px solid $dc-blue;
        }
}

li a  {
    font-size: .7rem;
    font-weight: bold;
    text-decoration: none;
    color: $blackText ;

        &.active {
            color: $dc-blue;
         
        }
       
}


</style>