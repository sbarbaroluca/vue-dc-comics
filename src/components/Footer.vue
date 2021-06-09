<template>
  <footer>
    <div class="container">
      <div class="footer-link">
        <ul>
            <li>Dc comics</li>
            <li><a href="">Characters</a></li>
            <li><a href="">Comics</a></li>
            <li><a href="">Movies</a></li>
            <li><a href="">Tv</a></li>
            <li><a href="">Games</a></li>
            <li><a href="">Videos</a></li>
            <li><a href="">News</a></li>
        </ul>
        <ul>
            <li>Dc</li>
            <li><a href="">Terms Of Use</a></li>
            <li><a href="">Privacy policy (New)</a></li>
            <li><a href="">Ad Choices</a></li>
            <li><a href="">Advertising</a></li>
            <li><a href="">Jobs</a></li>
            <li><a href="">Subscriptions</a></li>
            <li><a href="">Talent Workshops</a></li>
            <li><a href="">CSPS Certificates</a></li>
            <li><a href="">Ratings</a></li>
            <li><a href="">Shop Help</a></li>
            <li><a href="">Contact Us</a></li>
        </ul>  
        <ul>
            <li>Sites</li>
            <li><a href="">DC</a></li>
            <li><a href="">MAD Magazine</a></li>
            <li><a href="">DC Kids</a></li>
            <li><a href="">DC Universe</a></li>
            <li><a href="">DC Power Visa</a></li>  
        </ul>
        <ul>
            <li>Shop</li>
            <li><a href="">Shop DC</a></li>
            <li><a href="">Shop DC Collectibles</a></li>       
        </ul>
      </div>
      <div class="banner-container">
          <img src="../assets/img/dc-logo-bg.png" alt="" />
      </div>
    </div>
    <div class="social-bar">
        <div class="container">
          <button>Sign-up now!</button>
          <div class="social-link">
            <ul>
                <li>Follow us</li>      
                <li>
                    <img src="../assets/img/footer-facebook.png" alt="facebook" />
                </li>
                <li>
                    <img src="../assets/img/footer-twitter.png" alt="twitter" />
                </li>    
                <li>
                    <img src="../assets/img/footer-youtube.png" alt="youtube" />
                </li>    
                <li>
                    <img src="../assets/img/footer-pinterest.png" alt="pinterest" />
                </li>    
                <li>
                    <img src="../assets/img/footer-periscope.png" alt="periscope" />
                </li>   
            </ul>
          </div>
        </div>
    </div>                 
  </footer>
</template>

<script>
export default {
        name: "Footer"
};
</script>

<style lang="scss" scoped>
@import "../style/variables";
@import "../style/mixins";
footer {
  background: url("../assets/img/footer-bg.jpg") no-repeat;
  background-size: cover;
  overflow: hidden;
  .footer-link {
    display: inline-block;
    width: 35%;
    padding-top: 3%;
    &::after {
      @include clearfix;
    }
    ul {
      float: left;
      margin-right: 10%;
      &:last-child {
        position: relative;
        bottom: 100px;
      }
      li {
        color: #959595;
        margin: 10% 0;
        font-size: 12px;
        &:first-child {
        margin-bottom: 15%;
        text-transform: uppercase;
        color: #fff;
        font-size: 20px;
        font-weight: 600;
         }
      }
    }
  }
  .banner-container {
    position: relative;
    display: inline-block;
    width: 63%;
    text-align: right;
    & > img {
      position: absolute;
      right: 0;
      bottom: -30px;
      transform: scale(1.2);
    }
  }
  .social-bar {
    position: relative;
    z-index: 2;
    height: 150px;
    background-color: #303030;
    .container {
      @include flex-center("vertical");
      justify-content: space-between;
      height: 100%;
      .social-link {
        width: 50%;
        ul {
          @include flex-center("vertical");
          justify-content: flex-end;
          & > li {
            margin: 0 2%;
            cursor: pointer;
          &:first-child {
            color: $brandColor;
            text-transform: uppercase;
            font-weight: 700;
            font-size: 20px;
          }
          }
        }
      }
    }
  }
  }  
</style>