<script>
export default {
  name: 'AppMain',
  data(){
    return{
      menu:[
        {
          text: 'digital comics',
          href: '#'
        },
        {
          text: 'dc merchandise',
          href: '#'
        },
        {
          text: 'subscription',
          href: '#'
        },
        {
          text: 'comic shop locator',
          href: '#'
        },
        {
          text: 'dc power visa',
          href: '#'
        }
      ]
    }
  }
}
</script>

<template>
  <main>

    <section class="content">
      <div class="container">
        <h2>--> Content goes here</h2>
      </div>
    </section>

    <section>
      <div class="container">
        <nav>
          <ul>
            <li
            v-for="(link, index) in menu"
            :key="index"
            ><a :href="link.href">{{link.text}}</a></li>
          </ul>
        </nav>
      </div>
    </section>

  </main>
</template>

<style lang="scss" scoped>

@use '../style/general' as *;
@use '../style/partials/mixin' as *;

  .content {
    height: 130px;
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
    a{
      text-decoration: none;
      text-transform: uppercase;
      color: white;
    }
    }
  }

</style>