<template>
  <div class="menu">
    <div class="menu-wrapper">
      <div class="options">
        <ul>
          <li>Misja</li>
          <li>O swietone</li>
          <li>O mnie</li>
          <li>Portfolio</li>
          <li>Branding</li>
          <li>Współpraca</li>
        </ul>
      </div>
      <div class="divider">
        <img :src="divider" alt="divider-svg" />
      </div>
      <div class="info">
        <div class="contact">
          <h1>Kontakt</h1>
          <a href="mailto:czarnocki.w@wp.pl">czarnocki.w@wp.pl</a>
          <a href="mailto:czarnocki.w@wp.pl">kontakt@swietone.pl</a>
        </div>
        <div class="socials">
          <h2>Media</h2>
          <div class="links">
            <img :src="linkedInIcon" alt="linkedin-icon" />
            <img :src="gitIcon" alt="github-icon" />
            <img :src="behanceIcon" alt="behance-icon" />
          </div>
        </div>
      </div>
      <div class="menu-handler" @click="$emit('toggleMenu', false)">
        <div class="menu-kebab">
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
          <div class="circle"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      divider: require("../assets/svg/divider.svg"),
      linkedInIcon: require("../assets/svg/linkedin-icon.svg"),
      gitIcon: require("../assets/svg/git-icon.svg"),
      behanceIcon: require("../assets/svg/behance-icon.svg"),
    };
  },
};
</script>

<style scoped lang="scss">
@import "@/assets/_variables.scss";
.menu {
  width: 100vw;
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100vh;
  background-color: $champion-green;

  .menu-wrapper {
    display: flex;
    align-items: center;
    justify-content: space-around;
    padding: 2em;
  }
  .menu-handler {
    position: absolute;
    top: 6%;
    right: 3.5%;
  }

  ul {
    list-style-type: none;
    color: white;
    font-family: $libreBasker;
    font-size: 48px;
    line-height: 1.4em;

    li {
      border-bottom: 10px solid transparent;
      border-image: none;

      &:hover {
        border-image: url("../assets/svg/waves.svg") 100 stretch;
        transition: all 1000ms cubic-bezier(0.175, 0.885, 0.32, 1.275);
        cursor: pointer;
      }
    }
  }

  .info {
    display: flex;
    flex-direction: column;
    > div {
      margin: 2em 0;
    }

    .contact {
      h1 {
        font-size: 45px;
        font-family: $libreBasker;
        color: white;
        margin-bottom: 16px;
      }
      a {
        display: block;
        text-decoration: none;
        cursor: pointer;
        color: white;
        margin: 5px 0;
        font-family: $sourcePro;
        font-weight: 300;
      }
    }

    .socials {
      h2 {
        font-size: 40px;
        font-family: $libreBasker;
        color: white;
        margin-bottom: 16px;
      }

      .links {
        display: flex;
        justify-content: space-between;

        > img {
          max-width: 28px;
          cursor: pointer;

          &:hover {
            transform: scale(1.05);
            transition: all 1000ms cubic-bezier(0.175, 0.885, 0.32, 1.275);
          }
        }
      }
    }
  }
}
</style>
