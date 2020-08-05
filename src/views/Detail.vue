<template>
  <div class="container mt-3">
    <div class="row">
      <div class="col-12">
        <b-breadcrumb :items="breadcrumb" class="custom-breadcrumb"></b-breadcrumb>
      </div>
    </div>
    <div class="row">
      <div class="col-12">
        <h3>Cras maximus purus libero, non ullamcorper quam tincidunt at.</h3>
        <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus vestibulum lacinia luctus. Nullam venenatis hendrerit mi, eget scelerisque purus consectetur nec. Curabitur malesuada volutpat metus, sit amet viverra odio congue ac. Vivamus urna est, efficitur mollis pharetra nec, varius in lacus. Nam turpis tortor, tristique a lacus at, varius tristique elit. Ut tempor congue magna, in vestibulum eros finibus vitae. Nunc eu dolor lacinia, interdum lacus at, ultrices dolor. Praesent et luctus augue, non bibendum neque. Morbi laoreet mauris aliquam, sollicitudin purus convallis, pellentesque metus. Aenean pulvinar consectetur pretium.</p>
      </div>
    </div>
  </div>
</template>

<script>
import HeroSlider from '@/components/HeroSlider';
import SideMenu from '@/components/SideMenu';

export default {
  name: 'Home',
  components: {
    HeroSlider,
    SideMenu,
  },
  data: function(){
    return {
      items: [
        { id: 11, title: 'Lorem ipsum dolor', img: 'https://picsum.photos/600/300/?image=25'},
        { id: 12, title: 'Nunc ut augue', img: 'https://picsum.photos/600/300/?image=25'},
        { id: 13, title: 'Cras maximus purus', img: 'https://picsum.photos/600/300/?image=25'},
        { id: 14, title: 'Integer consequat', img: 'https://picsum.photos/600/300/?image=25'},
        { id: 15, title: 'Phasellus bibendum', img: 'https://picsum.photos/600/300/?image=25'}
      ],
      breadcrumb: [
        { text: 'Home', href: '/' },
        { text: 'Lorem ipsum dolor', active: true }
      ]
    };
  }
}
</script>

<style scoped>
  .custom-breadcrumb {
    border-radius: 0;
    background-color: #f7f7f7;
  }
  .custom-breadcrumb .breadcrumb-item a {
    color: #17a2b8;
  }
</style>