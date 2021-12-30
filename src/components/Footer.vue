<template>
  <footer class="footer">
    <div class="footer-wrapper">
      <div class="contact">
        <h4>
          Od <span>brandingu,</span><br />
          aż po <span>stronę!</span>
        </h4>
        <h5>swietone.</h5>
        <ul>
          <li>NIP: 5783130795</li>
          <li>kontakt@swietone.pl</li>
          <li>czarnocki.w@wp.pl</li>
          <li>Wojciech Czarnocki</li>
          <li>(+48) 513 192 155</li>
        </ul>
      </div>
      <div class="divider">
        <img :src="divider" alt="divider-svg" />
      </div>
      <div class="partnership">
        <h6>Współpraca?</h6>
        <p>
          Jeżeli są Państwo zainteresowani skorzystaniem z naszych usług,
          prosimy kontaktować się telefonicznie bądź mailowo. Z przyjemnością
          odpowiemy na wszelkie pytania i znajdziemy odpowiednie rozwiązanie.
        </p>
        <a href="tel:+48513192155"
          ><img :src="phoneCloud" alt="phone-cloud-svg"
        /></a>
        <a href="mailto:czarnocki.w@wp.pl"
          ><img :src="mailCloud" alt="mail-cloud-svg"
        /></a>
        <p class="company-p">
          powered by <span class="swietone">swietone.</span>
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      divider: require("../assets/svg/divider.svg"),
      phoneCloud: require("../assets/svg/phone-cloud.svg"),
      mailCloud: require("../assets/svg/mail-cloud.svg"),
    };
  },
};
</script>

<style lang="scss">
@import "@/assets/_variables.scss";

.footer {
  display: flex;
  align-items: center;
  height: 100vh;
  width: 100vw;
  position: relative;

  .footer-wrapper {
    display: flex;
    width: 100%;
    align-items: center;
    justify-content: space-around;
    padding: 2em;
  }

  .contact {
    font-family: $libreBasker;
    h4 {
      font-size: 36px;
      color: $white;
      line-height: 1.2;
      margin-bottom: 2em;
      text-align: right;

      > span {
        color: $croisant-yellow;
      }
    }

    h5 {
      color: $croisant-yellow;
      font-size: 28px;
    }

    ul {
      list-style-type: none;

      > li {
        margin: 10px 0;
        color: $white;
        font-family: $libreBasker;
        font-size: 15px;
      }
    }
  }

  .partnership {
    max-width: 40%;
    text-align: right;

    h6 {
      font-size: 50px;
      color: $white;
      margin-bottom: 0.5em;
      text-align: right;
    }

    p {
      display: block;
      font-family: $sourcePro;
      color: $white;
      font-weight: lighter;
      font-size: 20px;
      margin-bottom: 1em;
      // width: 80%;
    }

    a :hover {
      transform: scale(1.05);
      transition: all 1000ms cubic-bezier(0.175, 0.885, 0.32, 1.275);
      box-shadow: rgba(50, 50, 93, 0.25) 0px 13px 27px -5px,
        rgba(0, 0, 0, 0.3) 0px 8px 16px -8px;
    }
    a:first-of-type {
      margin-right: 1em;
    }

    .company-p {
      display: block;
      position: absolute;
      color: $white;
      font-size: 16px;
      font-family: $sourcePro;
      font-weight: lighter;
      line-height: 1.2;
      bottom: 5%;
      right: 8%;
      opacity: 50%;

      .swietone {
        font-family: $libreBasker;
        font-size: 16px;
        display: block;
      }
    }
  }
}
</style>
