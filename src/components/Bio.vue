<template>
  <section>
    <div class="bio">
      <div class="info">
        <h3>Wojciech Czarnocki</h3>
        <p>
          Od prawie 2 lat pracuję jako Junior Java Developer w LSEG, natomiast
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
section {
  height: 100vh;
  
  position: relative;

  .bio {
    // height: 100%;
    
    display: flex;
    align-items: center;
    // justify-content: center;

    .info {
      height: 100%;
        max-width: 50%;
        color: white;
        margin-top: 15%;
        padding: 2em 5em;
        
        h3 {
            font-family: "Libre Baskerville", serif;
            font-size: 30px;
        }

        p{
          font-family: "Source Sans Pro", sans-serif;
          margin: 1em 0;
          font-weight: 300;
          line-height: 1.2em;
          font-size: 18px;
          
        }

        .socials {
          
          img {
            max-width: 20px;
            margin-right: 1em;
          }
        }
    }

    .portrait {
      
        max-width: 50%;
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
