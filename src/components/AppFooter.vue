<template>
  <footer>
      <div class="foot">
          <div class="left">
              <div class="one">
                <h3>DC Comics</h3>
                <ul>
                    <li v-for="(item, index) in DCComics" :key="index">{{item}}</li>
                </ul>
                <h3>Shop</h3>
                <ul>
                    <li v-for="(item, index) in shop" :key="index">{{item}}</li>
                </ul>
              </div>

              <div class="two">
                  <h3>DC</h3>
                  <ul>
                    <li v-for="(item, index) in DC" :key="index">{{item}}</li>
                  </ul>
              </div>

              <div class="three">
                  <h3>sites</h3>
                  <ul>
                    <li v-for="(item, index) in DCComics" :key="index">{{item}}</li>
                  </ul>
              </div>
          </div>
            <img src="../assets/img/dc-logo-bg.png" alt="">
      </div>

      <div class="media">
          <button>Sing-Up Now!</button>

          <div class="right">
              <p>follow Us</p>
              <img v-for="(item, index) in footerImg" :src="item" alt="" :key="index">
          </div>
      </div>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
  data() {
    return {
      DCComics: ['Characters', 'Comics', 'Movies', 'TV', 'Games', 'Videos', 'News'],
      shop: ['Shop DC', 'Shop Collectibles'],
      DC: ['Terms Of Use', 'Privacy Policy(new)', 'Ad Choices', 'Advertising', 'Jobs', 'Subscriptions', 'Talent Workshop', 'CPSC Certificates', 'Ratings', 'Shop Help', 'Contact Us'],
      sites: ['DC', 'Mad Magazine', 'DC Kids', 'DC Universe', 'DC Power Visa'],
      footerImg: [require('../assets/img/footer-facebook.png'), require('../assets/img/footer-periscope.png'), require('../assets/img/footer-pinterest.png'), require('../assets/img/footer-twitter.png'),
      require('../assets/img/footer-youtube.png')]

    };
  },
};
</script>

<style scoped lang="scss">
    @import "../style/variables.scss";
    @import "../style/generals.scss";

    .foot{
        height: 300px;
        background-image: url('../assets/img/footer-bg.jpg');
        background-size: cover;
        display: flex;
        justify-content: space-around;
        align-items: center;
        overflow: hidden;

        .left{
            display: flex;
            gap: 20px;

            h3{
                text-transform: uppercase;
                font-weight: bold;
                color: white;
                margin-bottom: 20px;
            }

            ul{
                margin-bottom: 20px;

                li{
                    font-size: smaller;
                    color: $footer-color;
                }
            }
        }

        img{
            width: 450px;
        }
    }

    .media{
        height: 70px;
        background-color: $footer-bg;
        display: flex;
        justify-content: space-around;
        align-items: center;
        text-transform: uppercase;

        button{
            padding: 10px;
            background-color: $footer-bg;
            font-size: larger;
            color: white;
            border: 3px solid $text-color;
            text-transform: uppercase;
        }

        .right{
            display: flex;
            align-items: center;
            gap: 10px;

            p{
                font-size: larger;
                color: $text-color;
                font-weight: bolder;
            }

            img{
                width: 30px;
            }
        }
    }
</style>