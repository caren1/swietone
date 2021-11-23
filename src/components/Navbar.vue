<template>
  <nav class="navbar">
      <div class="logo">
        <img :src="swietoneHorizontalLogo" alt="swietone-main-logo"/>
      </div>
      <div class="menu">
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
      </div>
  </nav>
</template>

<script>
export default {
   data() {
       return {
           swietoneLogo: require('../assets/svg/swietone-main-logo.svg'),
            swietoneHorizontalLogo: require('../assets/svg/swietone-horizontal-logo.svg')
       }
   }
}
</script>

<style>

.navbar {
    padding: 2em 3em;
    background: transparent;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: white;
    
}

.logo {
    max-width: 140px;
}

.logo img {
    width: 100%;
}

.menu {
  flex-direction: column;
  position: relative;
  transition: all 300ms cubic-bezier(0.175, 0.885, 0.32, 1.275);
  .circle:nth-child(4),
  .circle:nth-child(5) {
    position: absolute;
    opacity: 0;
    top: 50%;
    margin-top: -6px;
    left: 50%;
  }
  .circle:nth-child(4) {
    margin-left: -25px;
  }
  .circle:nth-child(5) {
    margin-left: 13px;
  }
  &:hover,
  &:focus {
    transform: rotate(45deg);
    .circle {
      opacity: 1;
    }
  }
}
</style>