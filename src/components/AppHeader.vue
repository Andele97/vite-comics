<script>
export default {
  name: 'AppHeader',
  data(){
    return{
      menu:[
        {
          text: 'characters',
          href: '#',
          current: false
        },
        {
          text: 'comics',
          href: '#',
          current: false
        },
        {
          text: 'movies',
          href: '#',
          current: false
        },
        {
          text: 'tv',
          href: '#',
          current: false
        },
        {
          text: 'games',
          href: '#',
          current: false
        },
        {
          text: 'collectibles',
          href: '#',
          current: false
        },
        {
          text: 'videos',
          href: '#',
          current: false
        },
        {
          text: 'fans',
          href: '#',
          current: false
        },
        {
          text: 'news',
          href: '#',
          current: false
        },
        {
          text: 'shop',
          href: '#',
          current: false
        }
      ]
    }
  }
}
</script>

<template>

  <header>
    <div class="logo">
      <img src="../assets/img/dc-logo.png" alt="Logo Dc">
    </div>

    <nav>
      <ul>
        <li
        v-for="(link, index) in menu"
        :key="index"
        ><a :class="{'active': link.current}" :href="link.href">{{link.text}}</a></li>
      </ul>
    </nav>
  </header>

</template>

<style lang="scss" scoped>

@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;

header {
  height: 150px;
  @include centerFlex('between');
  ul{
    list-style: none;
    @include centerFlex('horizontal');
    a{
      text-decoration: none;
      margin-left: 30px;
      color: black;
      text-transform: uppercase;
      padding-bottom: 20px;
      &:hover,
      &:active{
        color: #0282F9;
        box-shadow: 0px 5px 0px 0px #0282F9;
      }
    }
  }
}

</style>