<script>

import CardComics from './CardComics.vue';
import datacomics from '../data/datacomics';

export default {
  name: 'AppMain',
  components: {
    CardComics
  },
  data(){
    return{
      datacomics,
      menu:[
        {
          text: 'digital comics',
          href: '#',
          icon: new URL('../assets/img/buy-comics-digital-comics.png', import.meta.url).href
        },
        {
          text: 'dc merchandise',
          href: '#',
          icon: new URL('../assets/img/buy-comics-merchandise.png', import.meta.url).href
        },
        {
          text: 'subscription',
          href: '#',
          icon: new URL('../assets/img/buy-comics-subscriptions.png', import.meta.url).href
        },
        {
          text: 'comic shop locator',
          href: '#',
          icon: new URL('../assets/img/buy-comics-shop-locator.png', import.meta.url).href
        },
        {
          text: 'dc power visa',
          href: '#',
          icon: new URL('../assets/img/buy-dc-power-visa.svg', import.meta.url).href
        }
      ]
    }
  }
}
</script>

<template>
  <main>

    <div class="jumbotron"></div>
    <section class="content">
      <div class="container">
        <div class="current">
          current series
        </div>
        <CardComics
        v-for="(card, index) in datacomics"
        :key="index"
        :cardImage="card.thumb"
        :cardTitle="card.series"
        />
      </div>
    </section>

    <section>
      <div class="container">
        <nav>
          <ul>
            <li
            v-for="(link, index) in menu"
            :key="index"
            ><img :src="link.icon"><a :href="link.href">{{link.text}}</a></li>
          </ul>
        </nav>
      </div>
    </section>

  </main>
</template>

<style lang="scss" scoped>

@use '../style/general' as *;
@use '../style/partials/mixin' as *;

  .jumbotron{
    height: 400px;
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
  }

  .content {
    background-color: #1C1C1C;
    @include centerFlex('vertical');
    h2{
      color: white;
    }
  }

  section:last-of-type{
    height: 155px;
    background-color: #0282F9;
    @include centerFlex('vertical');
    ul{
      list-style: none;
      @include centerFlex('evenly');
      @include centerFlex('vertical');
      li{
        text-align: center;
        @include centerFlex();
        img{
          width: 50px;
        }
        a{
          text-decoration: none;
          text-transform: uppercase;
          color: white;
          margin-left: 10px;
        }
      }
    }
  }

</style>