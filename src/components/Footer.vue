<template>
  <footer class="footer">
    <div class="contact">
      <h4>Od <span>brandingu</span><br />, aż po <span>stronę!</span></h4>
      <h5>swietone</h5>
      <ul>
        <li>NIP: 5783130795</li>
        <li>kontakt@swietone.pl</li>
        <li>czarnocki.w@wp.pl</li>
        <li>Wojciech Czarnocki</li>
        <li>(+48) 513 192 155</li>
      </ul>
    </div>
    <div class="divider"></div>
    <div class="partnership">
      <h6>Współpraca?</h6>
      <p>
        Jeżeli są Państwo zainteresowani skorzystaniem z naszych usług, prosimy
        kontaktować się telefonicznie bądź mailowo. Z przyjemnością odpowiemy na
        wszelkie pytania i znajdziemy odpowiednie rozwiązanie.
      </p>
      <a href="tel:+48513192155"
        ><img :src="phoneCloud" alt="phone-cloud-svg"
      /></a>
      <a href="mailto:czarnocki.w@wp.pl"
        ><img :src="mailCloud" alt="mail-cloud-svg"
      /></a>
      <span>powered by <span>swietone.</span></span>
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
.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 100vh;
  padding: 2em 4em;

  .contact {
    font-family: "Libre Baskerville", serif;
  }
}
</style>
