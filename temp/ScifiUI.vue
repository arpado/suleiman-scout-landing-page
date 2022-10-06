<template>
  <div class="ui-wrapper">
    <div class="ui-outer">
      <div class="ui-inner"></div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.ui-wrapper {
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
  filter: drop-shadow(0 0 15px var(--main-lightblue));
}
.ui-outer {
  height: fit-content;
  width: fit-content;
  /* padding: 1%; */
  background-color: var(--main-lightblue);
  /* background-color: hsla(180,100%,50%,0.6); */
 clip-path: polygon(7% 0, 50% 0, 53% 10%, 97% 10%, 100% 15%, 100% 30%, 97% 33%, 97% 60%, 100% 63%, 100% 90%, 95% 100%, 55% 100%, 52% 95%, 10% 95%, 0 82%, 0 50%, 2% 47%, 2% 17%);
  /* border: 2px solid var(--main-lightblue); */
  display: flex;
  justify-content: center;
  align-items: center;
}
.ui-inner {
  height: 90vh;
  width: 90vw;
  padding: 1%;
  background-color: var(--main-darkblue);
  /* background-color: hsla(180,100%,50%,0.6); */
  color: var(--main-white);
  font-weight: bold;
  font-size: 1.5rem;
  clip-path: polygon(6% 2%, 48% 2%, 51% 11%, 97% 11%, 99% 15%, 99% 31%, 97% 33%, 97% 60%, 100% 63%, 100% 90%, 95% 100%, 55% 100%, 52% 95%, 10% 95%, 0 82%, 0 50%, 2% 47%, 2% 17%, 2% 10%);
  white-space: nowrap;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
