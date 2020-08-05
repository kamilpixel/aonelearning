<template>
  <div>
    <b-card-group columns>
      <b-card
        v-for="item in items"
        v-bind:key= "item.id"
        :title="item.title"
        :img-src="getImgUrl(item.img)"
        img-top
        tag="article"
        style=""
        class="card-style mb-2"
      >
      <b-button variant="outline-primary" v-on:click="readMore">Read More</b-button>
      </b-card>
    </b-card-group>
  </div>
</template>

<script>
export default {
  name: 'cards',
  props: {
    items: Array
  },
  methods: {
    readMore(){
      this.$router.push('/detail');
    },
    getImgUrl(pic) {
      return require('../assets/'+pic);
    },
  },
}
</script>

<style scoped>
  .card-style {
    border-radius: 0;
  }

  .card-style .card-img-top {
    border-radius: 0;
  }

  .btn-outline-primary {
    color: #17a2b8;
    border-color: #17a2b8;
    border-radius: 0;
  }
  .btn-outline-primary:hover {
    color: #fff;
    background-color: #17a2b8;
  }
</style>