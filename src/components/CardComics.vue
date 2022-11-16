<script>
export default {
  name: 'CardComics',
  props: {
    cardImage: String,
    cardTitle: String
  }
};
</script>

<template>
  <div class="card">
    <div class="cover">
      <img :src="cardImage" :alt="cardTitle">
    </div>
    <h4>{{cardTitle}}</h4>
  </div>
</template>

<style lang="scss" scoped>
  .card{
    width: 200px;
    height: 200px;
    cursor: pointer;
    background-color: yellow;
    .cover{
      height: 120px;
      width: 120px;
      .img{
        width: 100%;
      }
    }
  }
</style>