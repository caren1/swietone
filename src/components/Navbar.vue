<template>
  <nav class="navbar">
      <div class="logo">
        <img :src="swietoneHorizontalLogo" alt="swietone-main-logo"/>
      </div>
      <div class="menu">
        <div class="menu-kebab">
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
        </div>  
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

<style lang="scss">

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
  height: 100%;
}

.circle {
  width: 6px;
  height: 6px;
  margin: 3px;
  background: #F8DA8F;
  border-radius: 50%;
  display: block;
}

.menu-kebab {
  flex-direction: column;
  position: relative;
  transition: all 300ms cubic-bezier(0.175, 0.885, 0.32, 1.275);
  .circle:nth-child(4),
  .circle:nth-child(5) {
    position: absolute;
    opacity: 0;
    top: 50%;
    margin-top: -3px; // here
    left: 50%;
  }
  .circle:nth-child(4) {
    margin-left: -12px; // here 
  }
  .circle:nth-child(5) {
    margin-left: 6px; // here
  }
  &:hover,
  &:focus {
    transform: rotate(45deg);
    .circle {
      opacity: 1;
      cursor: pointer;
    }
  }
}
</style>