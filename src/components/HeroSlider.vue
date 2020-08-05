<template>
  <div>
    <b-carousel
      :interval="4000"
      controls
      indicators
      background="#ababab"
      style="text-shadow: 1px 1px 2px #333;"
      class="custom-slider"
    >

      <b-carousel-slide
        v-for="slider in sliders"
        v-bind:key="slider.id"
        :caption="slider.caption"
        :img-src="getImgUrl(slider.img)"
      ></b-carousel-slide>

    </b-carousel>
  </div>
</template>

<script>
export default {
  name: 'HeroSlider',
  data: function() {
    return {
      sliders: [
        { id: 11, caption: 'Anyone Can Teach', img: 'images/sliders/slider1.jpg' },
        { id: 12, caption: 'Everyone Can Learn', img: 'images/sliders/slider2.jpg' },
      ]
    }
  },
  methods: {
    getImgUrl(pic) {
      return require('../assets/'+pic);
    }
  }
}
</script>

<style>
  .custom-slider .carousel-item img {
    height: 250px !important;
    width: 100%;
    object-fit: cover;
  }
</style>