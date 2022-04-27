<template>
  <div id="home">
    <Homie class="hero" />
  </div>
</template>

<script>
import Homie from './Homie.vue'
export default {
  name: "HomePage",
  components: { Homie }
};
</script>

<style scoped>
#home {
  width: 100%;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
#home::before {
  content: "";
  position: absolute;
  top: 0; left: 0;
  width: 100vw; height: 100vh;
  background-image: url("../assets/pattern/Reuss.svg");
  background-size: cover;
  filter:brightness(0.1);
  z-index: 0;
}
.hero {
  width: 80vw;
}
</style>