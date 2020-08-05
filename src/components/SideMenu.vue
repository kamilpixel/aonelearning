<template>
  <div>
    <b-list-group>
      <b-list-group-item button v-on:click="readMore">Programming</b-list-group-item>
      <b-list-group-item button v-on:click="readMore">Piano</b-list-group-item>
      <b-list-group-item button v-on:click="readMore">Baby Class</b-list-group-item>
      <b-list-group-item button v-on:click="readMore">Drawing</b-list-group-item>
      <b-list-group-item button v-on:click="readMore">Mandarin</b-list-group-item>
      <b-list-group-item button v-on:click="readMore">Ballet</b-list-group-item>
      <b-list-group-item button v-on:click="readMore">Other</b-list-group-item>
    </b-list-group>
  </div>
</template>
<script>
export default {
  methods: {
    readMore(){
      this.$router.push('/detail');
    },
  },
}
</script>


<style scoped>
  .list-group {
    border-radius: 0;
  }
  .list-group-item:hover {
    background-color: #17a2b8;
    color: #fff;
  }
</style>