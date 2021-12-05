<template>
  <section>
    <div class="bio">
      <div class="info">
        <h3>Wojciech Czarnocki</h3>
        <p>
          Obecnie pracuję jako Fullstack Developer w firmie Hapag Lloyd,
          wcześniej przez 2 lata pracowałem jako Junior Java Engineer, natomiast
          interesuję się również web developmentem jak i szeroko pojętym
          projektowaniem intefejsów użytkownika oraz designem.
        </p>
        <p>
          Moje realizacje wyróżniają się niestandarowym, nowoczesnym i
          minimalistycznym wyglądem, skrojonym pod oczekiwania klienta. Przy
          każdym projekcie dbam o każdy detal, dzięki czemu tworzę szybkie,
          zoptymalizowane i responsywne strony internetowe.
        </p>
        <p>
          Pracując nad każdym projektem, dobieram stosowne technologie, które w
          jak najlepszym stopniu sprostają wymaganiom.
        </p>
        <div class="socials">
          <img :src="linkedInIcon" alt="linkedin-icon" />
          <img :src="gitIcon" alt="github-icon" />
          <img :src="behanceIcon" alt="behance-icon" />
        </div>
      </div>
      <div class="portrait">
        <img :src="selfPortrait" alt="wojciech-czarnocki-portrait" />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      linkedInIcon: require("../assets/svg/linkedin-icon.svg"),
      gitIcon: require("../assets/svg/git-icon.svg"),
      behanceIcon: require("../assets/svg/behance-icon.svg"),
      selfPortrait: require("../assets/svg/me.svg"),
    };
  },
};
</script>

<style lang="scss">
@import "@/assets/_variables.scss";

section {
  height: 100vh;

  position: relative;

  .bio {
    display: flex;
    align-items: center;
    height: 100%;
    // padding: 1em 3em;

    .info {
      // height: 100%;
      max-width: 40%;
      color: white;
      margin-left: 10%;
      // margin-top: 15%;
      // padding: 2em 5em;

      h3 {
        font-family: $libreBasker;
        font-size: 34px;
      }

      p {
        font-family: $sourcePro;
        margin: 1em 0;
        font-weight: 300;
        line-height: 1.2em;
        font-size: 20px;
      }

      .socials {
        img {
          max-width: 20px;
          margin-right: 1em;
        }
      }
    }

    .portrait {
      max-width: 65%;
      position: absolute;
      bottom: 5%;
      right: 0;

      > img {
        width: 100%;
      }
    }
  }
}
</style>
