<script>
export default {
  name: 'AppFooter'
}
</script>

<template>
  <footer>
    <div class="footer-top">
      <div class="container">
        <div class="col">
      <h3>dc comics</h3>
      <ul>
        <li><a href="#">Characters</a></li>
        <li><a href="#">Comics</a></li>
        <li><a href="#">Movies</a></li>
        <li><a href="#">TV</a></li>
        <li><a href="#">Games</a></li>
        <li><a href="#">Videos</a></li>
        <li><a href="#">News</a></li>
      </ul>
      <h3>shops</h3>
      <ul>
        <li><a href="#">Shop DC</a></li>
        <li><a href="#">Shop DC Collectibles</a></li>
      </ul>
    </div>

    <div class="col">
      <h3>dc</h3>
      <ul>
        <li><a href="#">Terms Of Use</a></li>
        <li><a href="#">Privacy policy</a></li>
        <li><a href="#">Ad Choices</a></li>
        <li><a href="#">Advertising</a></li>
        <li><a href="#">Jobs</a></li>
        <li><a href="#">Subscriptions</a></li>
        <li><a href="#">Talent Workshops</a></li>
        <li><a href="#">CPSC Certificates</a></li>
        <li><a href="#">Ratings</a></li>
        <li><a href="#">Shop >Help</a></li>
        <li><a href="#">Contact Us</a></li>
      </ul>
    </div>

    <div class="col">
      <h3>sites</h3>
      <ul>
        <li><a href="#">DC</a></li>
        <li><a href="#">MAD Magazine</a></li>
        <li><a href="#">DC Kids</a></li>
        <li><a href="#">DC Universe</a></li>
        <li><a href="#">DC Power Visa</a></li>
      </ul>
    </div>
    
    <div class="logo">
      <img src="../assets/img/dc-logo-bg.png" alt="">
    </div>
    

    </div>

    <div class="footer-bottom">

    </div>
    </div>  
  </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

footer{
  color: $color-footer;
  background-color: lightgreen;
 

  .footer-top{
    background-image: url('../assets/img/footer-bg.jpg');
    background-repeat: no-repeat;
    height: 400px;
    overflow: hidden;

    .container{
      display: flex;
      position: relative;

      .col{
        margin-right: 30px;
        margin-bottom: 60px;
        @include menuStyle();

        h3{
          text-transform: uppercase;
          margin-top: 30px;
          margin-bottom: 13px;
        }

        a{
          color: grey;
          font-size: .9rem;
          line-height: 150%;
        }
       
      }

      .logo{
        position: absolute;
        right: 0;
        top: -60px;

      }
      

    }


  }

  
}


</style>