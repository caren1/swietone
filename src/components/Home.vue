<template>
  <div class="home">
    <div class="home-intro">
      <h1>Modernizacja strony <br/> internetowej lub brandingu?</h1>
      <h2> A może jeszcze nie masz strony?</h2>
      <a href="#">brzmi nieźle.</a>
      </div>
      <div class="home-waves">
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
@import url('https://fonts.googleapis.com/css2?family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&family=Source+Sans+Pro:ital,wght@0,200;0,300;0,400;0,600;0,700;1,200;1,300;1,400;1,600&display=swap');
.home {
  background-color: #0e483e;
  color: #ffffff;
  height: calc(100vh - 100px);
  padding: 0 3em;
  text-align: left;
  display: flex;
  flex-direction: column;
  justify-content: center;
  position: relative;
  
  
  .home-intro {
    margin-top: -5em;
    display: flex;
    flex-direction: column;
    padding: 0 2em;
  }

  h1 {
    font-size: 50px;
    margin-bottom: 0.5em;
    font-family: 'Libre Baskerville', serif;
    font-weight: lighter;
    line-height: 1.1em;
  }

  h2 {
    font-size: 30px;
    font-family: 'Source Sans Pro', sans-serif;
    margin-bottom: 0.5em;
    font-weight: 300;
  }

  a {
    margin-left: auto;
    text-decoration: none;
    font-size: 18px;
    color: white;
    font-family: 'Libre Baskerville', serif;
    font-weight: lighter;
    padding: 0.5em;
    border-bottom: 10px solid transparent;
    border-image: url('../assets/svg/waves.svg') 100 stretch;

    &:hover {
          border-image: url('../assets/svg/waves.svg') 200 stretch;
          transition: all 1000ms cubic-bezier(0.175, 0.885, 0.32, 1.275);

    }
  }

  .home-waves {
    position: absolute;
    overflow: hidden;
    left: 0;
    bottom: 0;
    height: 200px;
    // width: 100%;
              animation: move-forever 10s cubic-bezier(.55,.5,.45,.5) infinite;

    

    img {
          overflow: hidden;
          width: 100%;
    }
  }
}

@keyframes move-forever {
  0% {
   transform: translateY(0px);
  }
  50% { 
    transform: translateY(-20px);
  }
  100%{
    transform: translateY(0px);
  }
}

</style>
