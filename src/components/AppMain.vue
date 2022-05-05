<template>
  <main>
    <div class="jumbo"></div>

    <div class="box">
      <p class="current">current series</p>
      <app-card v-for="(item, index) in cards" :key="index" :link="item.thumb" :type="item.series"/>
      <button>load more</button>
    </div>

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
import AppCard from './AppCard.vue'

export default {
  name: "AppMain",
  components:{
    AppCard
  },
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
      cards: [
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
          price: "$19.99",
          series: "Action Comics",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
          price: "$3.99",
          series: "American Vampire 1976",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
          price: "$16.99",
          series: "Aquaman",
          type: "graphic novel",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
          price: "$2.99",
          series: "Batgirl",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$3.99",
          series: "Batman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
          price: "$2.99",
          series: "Batman Beyond",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
          price: "$3.99",
          series: "Batman/Superman",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
          price: "$4.99",
          series: "Batman/Superman Annual",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
          price: "$5.99",
          series: "Batman: The Joker War Zone",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
          price: "$6.99",
          series: "Batman: Three Jokers",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
          price: "$4.99",
          series: "Batman: White Knight Presents: Harley Quinn",
          type: "comic book",
        },
        {
          thumb:
            "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
          price: "$16.99",
          series: "Catwoman",
          type: "graphic novel",
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

  .jumbo {
    height: 400px;
    background-image: url("../assets/img/jumbotron.jpg");
    background-size: cover;
  }

  .box{
    height: 600px;
    width: 80%;
    margin: 0 auto;
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-content: center;
    gap: 30px;
    position: relative;

    .current{
      position: absolute;
      top: -20px;
      left: 20px;
      padding: 10px;
      font-size: larger;
      @include colorized
    }

    button{
      padding: 10px;
      font-size: large;
      border: 0px;
      @include colorized
    }
  }

  .info {
    height: 150px;
    background-color: $text-color;

    p {
    text-align: center;
    }

    ul {
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;

      li {
        height: 100%;
        margin-left: 20px;
        display: flex;
        align-items: center;
        @include colorized;

        p {
          line-height: 150px;
          margin-left: 5px;
        }

        img {
          width: 40px;
        }
      }
    }
  }
}
</style>