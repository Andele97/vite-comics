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
    <p>{{cardTitle}}</p>
  </div>
</template>

<style lang="scss" scoped>
  .card{
    margin-top: 30px;
    inline-size: 200px;
    padding: 0 30px 0;
    cursor: pointer;
    .cover{
      width: 150px;
      img{
        width: 100%;
      }
    }
    p{
      color: white;
      margin-top: 10px;
    }
  }
</style>