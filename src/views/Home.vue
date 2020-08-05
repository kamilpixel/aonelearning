<template>
  <div class="container">
    <div class="row">
      <div class="col-12">
        <HeroSlider />
      </div>
    </div>
    <div class="row mt-3">
      <div class="col-12 col-md-3 mb-3 mb-md-0">
        <SideMenu />
      </div>
      <div class="col-12 col-md-9">
        <Cards :items="items" />
      </div>
    </div>
  </div>
</template>

<script>
import HeroSlider from '@/components/HeroSlider';
import SideMenu from '@/components/SideMenu';
import Cards from '@/components/Cards';

export default {
  name: 'Home',
  components: {
    HeroSlider,
    SideMenu,
    Cards
  },
  data: function(){
    return {
      items: [
        { id: 11, title: 'Lorem ipsum dolor', img: 'images/cards/sample1.jpg'},
        { id: 12, title: 'Nunc ut augue', img: 'images/cards/sample2.jpg'},
        { id: 13, title: 'Cras maximus purus', img: 'images/cards/sample3.jpg'},
        { id: 14, title: 'Integer consequat', img: 'images/cards/sample4.jpg'},
        { id: 15, title: 'Phasellus bibendum', img: 'images/cards/sample5.jpg'}
      ]
    };
  }
}
</script>
