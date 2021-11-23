<template>
  <div class="about">
    <div class="about-waves">
      <img :src="waves" alt="waves-svg" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      waves: require("../assets/svg/waves.svg"),
    };
  },
};
</script>

<style scoped lang="scss">
.about {
  height: 100vh;
  position: relative;
    overflow: hidden;
    padding: 0 4em;


}
.about-waves {
  position: relative;
  overflow: hidden;
  left: -4em;
  
  width: 100vw;
  overflow: hidden;


  animation: move-forever 10s cubic-bezier(0.55, 0.5, 0.45, 0.5) infinite;

  img {
    overflow: hidden;
    width: 100%;
  }
}

@keyframes move-forever {
  0% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(10px);
  }
  100% {
    transform: translateY(0px);
  }
}
</style>
