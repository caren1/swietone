<template>
  <section class="home">
    <div class="home-intro">
      <h1>
        Modernizacja strony <br />
        internetowej lub brandingu?
      </h1>
      <h2>A może jeszcze nie masz strony?</h2>
      <a href="#">brzmi nieźle.</a>
    </div>
    <div class="home-waves">
      <img :src="waves" alt="waves-svg" />
    </div>
  </section>
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
@import "@/assets/_variables.scss";

.home {
  color: $white;
  min-height: calc(100vh - 100px);
  height: 100%;
  padding: 0 4em;
  text-align: left;
  display: flex;
  flex-direction: column;
  justify-content: center;
  position: relative;

  .home-intro {
    display: flex;
    flex-direction: column;
    padding: 3em 5em 2em 5em;
  }

  h1 {
    font-size: 50px;
    margin-bottom: 0.5em;
    font-family: $libreBasker;
    font-weight: lighter;
    line-height: 1.1em;
  }

  h2 {
    font-size: 30px;
    font-family: $sourcePro;
    margin-bottom: 0.5em;
    font-weight: 300;
  }

  a {
    margin-left: auto;
    text-decoration: none;
    font-size: 18px;
    color: white;
    font-family: $libreBasker;
    font-weight: lighter;
    padding: 0.3em;
    border-bottom: 10px solid transparent;
    border-image: url("../assets/svg/waves.svg") 100 stretch;

    &:hover {
      transform: scale(1.1);
      border-image: url("../assets/svg/waves.svg") 200 stretch;
      transition: all 1000ms cubic-bezier(0.175, 0.885, 0.32, 1.275);
    }
  }

  .home-waves {
    position: relative;
    overflow: hidden;
    left: -4em;
    bottom: -5em;
    width: 100vw;
    animation: move-forever 10s cubic-bezier(0.55, 0.5, 0.45, 0.5) infinite;
    overflow: hidden;

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
  75% {
    transform: translateY(10px);
  }
  100% {
    transform: translateY(0px);
  }
}
</style>
