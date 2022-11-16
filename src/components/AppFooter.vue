<script>
export default {
  name: 'AppFooter'
}
</script>

<template>
  <footer>

    <div class="footer-up">
      <div class="container">
        <div class="cont-link">
          <div class="link">
            <nav>
              <ul>
                <h4>dc comics</h4>
                <li><a href="#">Characters</a></li>
                <li><a href="#">Comics</a></li>
                <li><a href="#">Movies</a></li>
                <li><a href="#">TV</a></li>
                <li><a href="#">Games</a></li>
                <li><a href="#">Videos</a></li>
                <li><a href="#">News</a></li>
              </ul>
            </nav>
          </div>
          <div class="link">
            <nav>
              <ul>
                <h4>shop</h4>
                <li><a href="#">Shop DC</a></li>
                <li><a href="#">Shop DC Collectibles</a></li>
              </ul>
            </nav>
          </div>
          <div class="link">
            <nav>
              <ul>
                <h4>dc</h4>
                <li><a href="#">Terms Of Use</a></li>
                <li><a href="#">Privacy policy (New)</a></li>
                <li><a href="#">Ad Choices</a></li>
                <li><a href="#">Advertising</a></li>
                <li><a href="#">Jobs</a></li>
                <li><a href="#">Subscriptions</a></li>
                <li><a href="#">Talent WorkShops</a></li>
                <li><a href="#">CPSC Certificates</a></li>
                <li><a href="#">Ratings</a></li>
                <li><a href="#">Shop Help</a></li>
                <li><a href="#">Contact Us</a></li>
              </ul>
            </nav>
          </div>
          <div class="link">
            <nav>
              <ul>
                <h4>sites</h4>
                <li><a href="#">DC</a></li>
                <li><a href="#">MAD Magazine</a></li>
                <li><a href="#">DC Kids</a></li>
                <li><a href="#">DC Universe</a></li>
                <li><a href="#">DC Power Visa</a></li>
              </ul>
            </nav>
          </div>
        </div>
      </div>
    </div>

    <div class="footer-bottom">
      <div class="container">
        <div class="sign-up">
          sign up
        </div>
        <div class="follow-us">
          follow us
          <img src="../assets/img/footer-facebook.png" alt="">
          <img src="../assets/img/footer-twitter.png" alt="">
          <img src="../assets/img/footer-youtube.png" alt="">
          <img src="../assets/img/footer-pinterest.png" alt="">
          <img src="../assets/img/footer-periscope.png" alt="">
        </div>
      </div>  
    </div>
  </footer>
</template>

<style lang="scss" scoped>

@use '../style/general' as *;
@use '../style/partials/mixin' as *;

  .footer-up{
    height: 370px;
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;
    .container{
      @include centerFlex('between');
      height: 100%;
      background-image: url(../assets/img/dc-logo-bg.png);
      background-repeat: no-repeat;
      background-position: right; 
      .cont-link{
        display: flex;
        flex-wrap: wrap;
        flex-direction: column;
        height: 300px;
        .link{
          margin-top: 20px;
          margin-right: 20px;
          h4{
            color: white;
            text-transform: uppercase;
            margin-bottom: 10px;
            font-size: 1.3em;
          }
          ul{
            list-style: none;
            a{
              text-decoration: none;
              color: #777D73;
              font-size: 0.8em;
              &:hover{
                text-decoration: underline;
              }
            }
          }
        }
      }
    }
  }

  .footer-bottom {
    height: 110px;
    background-color: #303030;
    .container{
      height: 100%;
      @include centerFlex('between');
      .sign-up{
        padding: 20px;
        width: 150px;
        border: 4px solid #0282F9;
        text-transform: uppercase;
        color: white;
        text-align: center;
        cursor: pointer;
      }
    }
    .follow-us{
      color: #0282F9;
      text-transform: uppercase;
      font-weight: bold;
      display: flex;
      align-items: center;
      font-size: 1.2em;
      img{
        margin-left: 10px;
        cursor: pointer;
      }
    }
  }
</style>