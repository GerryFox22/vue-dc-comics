<template>
  <footer>
      <div class="footer-nav">
        <div class="footer-nav-elements">
            <div class="nav-menu">
              <div class="footer-nav-column">
                <h3>DC COMICS</h3>
                <ul>
                  <li v-for="(link, index) in dcComics" :key="index">
                    <a :href="'#'+ dcComics[index] "> {{ dcComics[index] }}</a>
                  </li>
                </ul>

                <h3>SHOP</h3>
                <ul>
                  <li v-for="(link, index) in shop" :key="index">
                    <a :href="'#'+ shop[index] "> {{ shop[index] }}</a>
                  </li>
                </ul>
              </div>

              <div class="footer-nav-column">
                <h3>DC</h3>
                <ul>
                  <li v-for="(link, index) in dc" :key="index">
                    <a :href="'#'+ dc[index] "> {{ dc[index] }}</a>
                  </li>
                </ul>
              </div>

              <div class="footer-nav-column">
                <h3>SITES</h3>
                <ul>
                  <li v-for="(link, index) in sites" :key="index">
                    <a :href="'#'+ sites[index] "> {{ sites[index] }}</a>
                  </li>
                </ul>
              </div>

            </div>

          <div class="footer-dc-logo">
            
          </div>

        </div>
      </div>

      <div class="footer-socials">
        <div class="footer-socials-container">
          <div class="follow-button">
            <button>SIGN-UP NOW!</button>
          </div>

          <div class="socials-dc">
            <h3>FOLLOW US</h3>
            <div v-for="(social,index) in socials" :key="index" class="singlge-dc-social">
              <a :href="social.url">
                <img :src="social.src" :alt="social.alt">
              </a>
            </div>
          </div>
        </div>
          
      </div>

  </footer>
</template>

<script>
export default {
    name: "Footer",

    data: function() {
      return {
        dcComics : ["Characters","Comics","Movies","TV","Games","Videos","News"],
        shop : ["Shop DC","Shop DC Collectibles"],
        dc : ["Terms Of Use","Privacy policy (New)","Ad Choices","Advertising","Jobs","Subscriptions","Talent Workshops","CPSC Certificates", "Ratings","Shop Help","Contact Us"],
        sites : ["DC","MAD Magazine","DC Kids","DC Universe","DC Power Visa"],

        socials : [
          {
            src : "./img/footer-facebook.png",
            alt : "Facebook image",
            url : "#DC-Facebook"
          },
          {
            src : "./img/footer-twitter.png",
            alt : "Twitter image",
            url : "#DC-Twitter"
          },
          {
            src : "./img/footer-youtube.png",
            alt : "Youtube image",
            url : "#DC-Youtube"
          },
          {
            src : "./img/footer-pinterest.png",
            alt : "Pinterest image",
            url : "#DC-Pinterest"
          },
          {
            src : "./img/footer-periscope.png",
            alt : "Periscope image",
            url : "#DC-Periscope"
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

.footer-nav {
  background-image: url("../assets/footer-bg.jpg");
  height: 300px;
}

.footer-dc-logo {
    background-image: url(/img/dc-logo-bg.f4404ce9.png);
    width: 40%;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
}

.nav-menu {
  display: flex;
  padding: 30px 0;
}

.footer-nav-elements {
  width: 80%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  height: 100%;
}

.footer-socials {
  background-color: #303030;
  display: flex;
}

.footer-nav-column {
  padding-right: 35px;
}

.footer-socials-container{
  width: 80%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  padding: 20px;
}

.socials-dc h3 {
  color: $dc-blue;
  margin: 0;
  margin-right: 10px;
}

.follow-button {
  margin-top: 10px;
}

.follow-button button {
  background-color: transparent;
  border: 1px solid $dc-blue;
  color: $whiteText;
  padding: 10px;
  cursor: pointer;
}

.socials-dc {
  display: flex;
  align-items: center;
}

.singlge-dc-social {
  padding: 10px;
}

h3 {
  color: $whiteText;
  font-size: .8rem;
  margin-bottom: 10px;
  margin-top: 0;
}

ul {
  margin: 0;
  padding: 0;
  line-height: 15px;
  margin-bottom: 20px;
}

ul li {
  list-style: none;
}

a {
  text-decoration: none;
  color: $grayText;
  font-size: .6rem;
}



</style>