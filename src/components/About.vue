<template>
  <div class="about">
      <div class="about-waves">
          <img :src="waves" alt="waves-svg">
      </div>
  </div>
</template>

<script>
export default {
   data() {
       return {
           waves: require('../assets/svg/waves.svg'),
       }
   }
}
</script>

<style scoped lang="scss">
    .about {
        height: 100vh;
        position: relative;
    }
    .about-waves {
    position: absolute;
    overflow: hidden;
    left: 0;
    top: 2%;
    height: 200px;
animation: move-forever 10s cubic-bezier(.55,.5,.45,.5) infinite;
    // width: 100%;

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
  100%{
    transform: translateY(0px);
  }
}

</style>