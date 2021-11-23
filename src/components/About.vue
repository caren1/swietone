<template>
  <div class="about">
    <div class="about-waves">
      <img :src="waves" alt="waves-svg" />
    </div>
    <div class="about-info">
      <div class="faded-circle"></div>
      <div class="info-details">
        <h1>Co możemy dla Ciebie zrobić?</h1>
        <ul>
          <li>zaprojektować branding</li>
          <li>odświeżyć wizerunek twojej działalności</li>
          <li>stworzyć nowoczesną stronę internetową</li>
          <li>przygotować dla niej unikalny szablon</li>
          <li>zadbać o odpowiedni UX</li>
          <li>zoptymalizować ją pod przeglądarki</li>
          <li>zmodernizować twoją istniejącą stronę</li>
        </ul>
      </div>
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
@import url("https://fonts.googleapis.com/css2?family=Libre+Baskerville:ital,wght@0,400;0,700;1,400&family=Source+Sans+Pro:ital,wght@0,200;0,300;0,400;0,600;0,700;1,200;1,300;1,400;1,600&display=swap");

.about {
  height: 100vh;
  position: relative;
  overflow: hidden;

  .about-waves {
    position: relative;
    overflow: hidden;
    z-index: 1;

    width: 100vw;
    overflow: hidden;
    animation: move-forever 10s cubic-bezier(0.55, 0.5, 0.45, 0.5) infinite;

    img {
      overflow: hidden;
      width: 100%;
    }
  }
  .about-info {
    width: 100%;
    height: 80%;
    display: flex;
    align-items: center;
    justify-content: center;

    .faded-circle {
      width: 700px;
      height: 700px;
      flex: 1;
      float: left;
      background: linear-gradient(
        0deg,
        rgba(2, 0, 36, 1) 0%,
        rgba(14, 72, 62, 1) 0%,
        rgba(248, 218, 143, 1) 100%
      );
      border-radius: 100%;
      float: right;
      shape-outside: circle(50%);
      position: absolute;
      left: -10%;
      z-index: 0;
    }

    ul {
      // list-style-type: disc;
      list-style-image: url('../assets/svg/list-style-circle.svg') !important;
      // overflow: hidden;
      float: left;
      margin-left: 2em;
      // shape-outside: circle(50%);
      // width: 200px;
      // height: 200px;
    }

    li {
      display: list-item;
      font-size: 20px;
      font-family: "Source Sans Pro", sans-serif;
      color: white;
      font-weight: 200;
      line-height: 2em;
    }
  }
  .info-details {
    z-index: 1;
    padding: 1em 2em;
    position: relative;
    left: 20%;

    h1 {
        font-family: "Libre Baskerville", serif;
        color: white;
        margin-bottom: 1em;
        font-size: 32px;
  
    }
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
