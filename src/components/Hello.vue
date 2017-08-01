<template>

  <div class="container">
    <md-card v-for="picture in pictures">
      <md-card-media>
        <img :src="picture.url" :alt="picture.title">
      </md-card-media>

      <md-card-content>
        {{picture.info}}
      </md-card-content>
    </md-card>
  </div>

</template>

<script>
  import data from '../data';

export default {
  name: 'hello',
  data () {
    return {
      pictures: data.pictures
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
  color: #35495E;
}

  .container {
    margin: 0 auto;
    max-width: 600px;
  }
</style>
