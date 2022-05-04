<template>
  <main>
    <p class="placeholder">-->Content goes here</p>

    <div class="info">
      <ul>
        <li v-for="(item, index) in infoList" :key="index">
          <img :src="item.img" alt="item.cosa" />
          <p>{{ item.cosa }}</p>
        </li>
      </ul>
    </div>
  </main>
</template>

<script>
export default {
  name: "AppMain",
  data() {
    return {
      infoList: [
        {
          cosa: "Digital Comics",
          img: require("../assets/img/buy-comics-digital-comics.png"),
          svg: false,
        },
        {
          cosa: "DC Merchandise",
          img: require("../assets/img/buy-comics-merchandise.png"),
          svg: false,
        },
        {
          cosa: "Subscription",
          img: require("../assets/img/buy-comics-subscriptions.png"),
          svg: false,
        },
        {
          cosa: "Comic Shop Locator",
          img: require("../assets/img/buy-comics-shop-locator.png"),
          svg: false,
        },
        {
          cosa: "DC Power Visa",
          img: require("../assets/img/buy-dc-power-visa.svg"),
          svg: true,
        },
      ],
    };
  },
};
</script>

<style scoped lang="scss">
    @import "../style/variables.scss";
    @import "../style/generals.scss";
    main {
        background-color: hsl(0deg 0% 11%);

        p {
            text-align: center;
            color: white;
        }

        .placeholder {
            line-height: 150px;
        }

        .info {
            height: 150px;
            background-color: $text-color;

            ul{
                height: 100%;
                display: flex;
                justify-content: center;
                align-items: center;

                li{
                    height: 100%;
                    margin-left: 20px;
                    display: flex;
                    align-items: center;
                    text-transform: uppercase;

                    p{
                        line-height: 150px;
                        margin-left: 5px;
                    }

                    img{
                        width: 40px;
                    }
                }
            }
        }
    }
</style>