<template>
  <header>
      <img src="../assets/img/dc-logo.png" alt="DC Logo">
      <nav>
          <ul>
              <li>
                  <a href="#">CHARACTER</a>
              </li>

              <li>
                  <a href="#">COMICS</a>
              </li>

              <li>
                  <a href="#">MOVIES</a>
              </li>

          </ul>
      </nav>
  </header>
</template>

<script>
export default {

}
</script>

<style Lang="SCSS" scoped>
@import "../style/variables.scss";

header {
    display: flex;
}

img{
    width:90px;
}

ul {
    display: flex
}

ul li {
    padding: 20px;
    list-style: none;
    
}

li a  {
    font-size: .7rem;
    font-weight: bold;
    text-decoration: none;
    color: black;
}


</style>