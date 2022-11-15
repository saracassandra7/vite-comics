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

    
    </div> 

    <div class="footer-bottom">
      <div class="sign-up">
        <div class="container">
          <h4>SIGN UP NOW!</h4>

          <div class="social">
            <h3>FOLLOW US</h3>
            <img src="../assets/img/footer-facebook.png" alt="facebook" />
            <img src="../assets/img/footer-twitter.png" alt="twitter" />
            <img src="../assets/img/footer-youtube.png" alt="youtube" />
            <img src="../assets/img/footer-pinterest.png" alt="pinterest" />
            <img src="../assets/img/footer-periscope.png" alt="periscope" />
          </div>
        </div>
      </div>

    </div> 
  </footer>
</template>

<style lang="scss" scoped>
@use '../styles/partials/mixin' as *;
@use '../styles/partials/variables' as *;

footer{
  color: $color-footer;

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

  .footer-bottom{

    .sign-up{
      background-color: #303030;
      height: 85px;
      @include centerFlex('vertical');


      .container{
        @include centerFlex('vertical');
        justify-content: space-between;

        h4{
          padding: 13px 20px;
          border: 2px solid $main-blue;
          cursor: pointer;
        }

        .social{
          @include centerFlex('vertical');

          h3{
            color: $main-blue;
            margin-right: 10px;
          }

          img{
            margin-left: 15px;
          }
        }
        
      }
    }
  }
  
}

</style>