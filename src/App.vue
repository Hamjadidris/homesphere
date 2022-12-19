<script>
import Nav from './components/Nav.vue';
import Intro from './components/intro.vue';
import Card from './components/card.vue';

export default {
  name: 'App',
  components: {
    Nav,
    Intro,
    Card,
  },
}
</script>

<template>
  <div class='app min-h-screen font-SofiaPro w-screen overflow-x-hidden'>

    <Nav />

    <img src="./assets/img/sprite.svg" class="w-1/12 absolute  top-20 -right-2 z-40" />

    <Intro />

    <img src="./assets/img/sprite.svg" class="w-1/12 absolute z-40" />

    <div class="cards flex justify-center space-x-10 relative top-24 md:static md:mt-16">
      <Card stat="90%" img="⌂" text='Already Inhabited' />
      <Card stat="50k" img='☺︎' text='Satisfied Customers' />
    </div>

    <img src="./assets/img/sprite.svg" class="w-1/12 absolute bottom-10 right-5 z-40" />
  </div>
</template>

<style scoped>
.app {
  position: relative;
}

.app::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: url(./assets/img/blueHouse-m.jpg);
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  filter: brightness(50%);
  clip-path: polygon(100% 0, 100% 85%, 81% 98%, 0 73%, 0 0);
}
</style>


