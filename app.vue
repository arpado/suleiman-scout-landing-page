<template>
  <div class="wrapper">
    <header>
      <!-- <img src="images/bg-stars.jpg" alt="" class="background" /> -->
      <img src="/images/red-giant.png" alt="" class="foreground" />
      <img src="/images/scout.png" alt="" class="ship" />
      <div class="hero-text"> 
        <h1>FLY FREE!</h1>
        <h2>Quality. Tradition. Reliability.</h2>
        <h2>Suleiman.</h2>
      </div>
      <div class="call-to-action-wrapper">
        <div class="call-to-action-box">
          <div class="call-to-action">
            <p>Take a Step!</p>
          </div>
        </div>
      </div>
    </header>
    <section>
      <!-- <AugmentedUI>
        <NuxtChild />
      </AugmentedUI> -->
      <!-- <ScifiUI /> -->
      <!-- <NuxtLayout :name="augmented">
        <div>placeholder</div>
      </NuxtLayout> -->
      <Augmented />
    </section>

    <!-- <section>
        <div class="sci-fi-ui-wrapper">

        </div>
    </section>-->
  </div> 
</template>

<script>

export default {
};
</script>

<style>
@import "/node_modules/augmented-ui/augmented-ui.min.css";

:root {
  --main-darkblue: #285278;
  --main-lightblue: #afd3ff;
  --main-yellow: #e09f20;
  --main-white: #f1f1e6;
  --main-black: #303437;
}
body {
  margin: 0;
}
.hero-text {
  position: absolute;
  top: 20vh;
  right: 10vw;
   color: var(--main-white);
}
h1 {
  font-size: 3rem;
  text-shadow: 0 0 5px rgb(5, 5, 5);
}
h2 {
  font-size: 2rem;
}
/* Ez a kov par sor csinlja a parat */
.wrapper {
  height: 100vh;
  overflow-y: auto;
  overflow-x: hidden;
  perspective: 10px;
  background-image: url('/images/bg-stars.jpg');
  background-size: cover;
}
header {
  position: relative;
  display: flex;
  justify-content: flex-start;
  align-items: flex-end;
  height: 100%;
  transform-style: preserve-3d;
  z-index: -1;
}
.background {
  position: absolute;
  /* height: 100%; */
  height: 100%;
  width: 100%;
  object-fit: cover;
  z-index: -1;
  transform: translateZ(-19px) scale(3);
}
.foreground {
  position: absolute;
  height: 50%;
  object-fit: fill;
  z-index: -1;
  transform: translateZ(-5px) scale(1.5);
  margin-bottom: 20vh;
}
.ship {
  margin-left: 25vw;
  margin-bottom: 25vh;
  transform: translateZ(5px) scale(0.8);
}
.call-to-action {
    /* position: absolute; */
    /* top: 80vh; */
    /* right: 20vw; */
    height: 50px;
    width: 200px;
    padding: 1%;
    background-color: var(--main-darkblue);
    /* background-color: hsla(180,100%,50%,0.6); */
    color: var(--main-white);
    font-weight: bold;
    font-size: 1.5rem;
    clip-path: polygon(10% 0, 100% 0, 100% 50%, 90% 100%, 0 100%, 0 50%);
    border: 2px solid var(--main-lightblue);
    white-space: nowrap;
     display: flex;
    justify-content: center;
    align-items: center;
}
.call-to-action-box{
    /* position: absolute;
    top: 80vh;
    right: 20vw; */
    height: fit-content;
    width: fit-content;
    /* padding: 1%; */
    background-color: var(--main-lightblue);
    /* background-color: hsla(180,100%,50%,0.6); */
    clip-path: polygon(10% 0, 100% 0, 100% 50%, 90% 100%, 0 100%, 0 50%);
    border: 2px solid var(--main-lightblue);
    display: flex;
    justify-content: center;
    align-items: center;
}
.call-to-action-wrapper {
    position: absolute;
    top: 80vh;
    right: 20vw;
       /* height: fit-content;
      width: fit-content; */
    display: flex;
    justify-content: center;
    align-items: center;
    filter: drop-shadow(0 0 15px var(--main-lightblue));
}
.call-to-action-box:hover {
    cursor: pointer;
    box-shadow: 0 0 5px var(--main-lightblue);
}
section {
  font-size: 2rem;
  /*padding: 2.5vh 2.5vw;
   background: #333; */
  /* background-image: url('/images/bg-stars.jpg'); */
  background-size: cover;
  height: 100vh;
  width: 100vw;
  /* margin-top: 300px; */
   display: flex;
    justify-content: center;
    align-items: center;
}
</style>
