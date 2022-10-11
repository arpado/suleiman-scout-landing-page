<template>
  <!-- <div class="big-wrapper"> -->
  <div class="filter">
    <div
      class="console-wrapper"
      data-augmented-ui="
  tl-clip tr-2-clip-x r-clip-y br-clip-x b-clip-x bl-clip l-clip-y both
"
    >
      <div class="box">
        <!-- <slot /> -->
        <!-- <router-view ></router-view> -->
        <!-- <NuxtChild /> -->
        <swiper
          class="swiper"
          :slides-per-view="1"
          :space-between="0"
          @swiper="onSwiper"
          @slideChange="onSlideChange"
        >
          <swiper-slide><SpecsSection /></swiper-slide>
          <swiper-slide><ShowcaseSection /></swiper-slide>
          <swiper-slide><OrderSection /></swiper-slide>
        </swiper>
      </div>

      <div class="btns">
        <NuxtLink to="/SpecsSection" class="nuxt-link">
          <div class="btn" data-augmented-ui="all-hexangle-up border">1</div>
        </NuxtLink>
        <nuxt-link to="" class="nuxt-link">
          <div class="btn" data-augmented-ui="all-hexangle-down border">2</div>
        </nuxt-link>
        <nuxt-link to="" class="nuxt-link">
          <div class="btn" data-augmented-ui="all-hexangle-up border">3</div>
        </nuxt-link>
      </div>
    </div>
  </div>
  <!-- <div class="little-thigy"></div>
</div> -->
</template>

<script>
// import SpecsSection from './SpecsSection.vue';
  // Import Swiper Vue.js components
  import { Swiper, SwiperSlide } from 'swiper/vue';

  // Import Swiper styles
  import 'swiper/css';

export default {
  components: {
      Swiper,
      SwiperSlide,
    },
    setup() {
      const onSwiper = (swiper) => {
        console.log(swiper);
      };
      const onSlideChange = () => {
        console.log('slide change');
      };
      return {
        onSwiper,
        onSlideChange,
      };
    },
};
</script>

<style scoped>
.console-wrapper {
  height: 95vh;
  width: 95vw;
  /* background: var(--main-lightblue); */
  --aug-tl: 5%;
  --aug-tr: 50px;
  --aug-tr-extend1: 60%;
  --aug-r-extend1: 40%;
  --aug-r-center: 50%;
  --aug-r1: 25px;
  --aug-r2: 25px;
  --aug-bl: 100px;
  --aug-br: 30px;
  --aug-b-extend1: 25%;
  --aug-l-extend1: 20%;
  --aug-l-center: 35%;
  --aug-l1: 25px;
  --aug-l2: 25px;
  --aug-inlay-all: 0px;
  --aug-inlay-bg: var(--main-darkblue);
  --aug-inlay-opacity: 40%;
  --aug-border-all: 10px;
  --aug-border-bg: var(--main-lightblue);
  --aug-border-opacity: 60%;
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
}
.filter {
  filter: drop-shadow(0 0 10px var(--main-lightblue));
  display: flex;
  justify-content: center;
  align-items: center;
  /* grid */
  /* grid-row: 1/13;
  grid-column: 1/13; */
}
/* .little-thigy {
    width: 50px;
    height: 50px;
    background: var(--main-lightblue);
  grid-row: 6/7;
  grid-column: 11/12;
}
.big-wrapper {
      display: grid;
      grid-template-columns: repeat(12, 1fr);
      grid-template-rows: repeat(12, 1fr);

} */
.box {
  width: 85%;
  height: 75%;
  /* background: red; */
  /* position: absolute;
    top: 10%;
    left: 10%; */
  border: 1px solid var(--main-lightblue);
  overflow-y: scroll;
}
.swiper {
  width: 100%;
  height: 100%;
  overflow-y: auto;
}
.btns {
  width: 85%;
  height: 10%;
  /* background: green; */
  display: flex;
  justify-content: flex-end;
  align-items: center;
}
.btn {
  --aug-all-width: 70px;
  --aug-border-bg: var(--main-lightblue);
  background: var(--main-darkblue);
  display: flex;
  justify-content: center;
  align-items: center;
  color: var(--main-white);
  text-shadow: 0 0 5px var(--main-white);
}
.nuxt-link {
  text-decoration: none;
}
</style>