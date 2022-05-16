<template>
  <section id="contact">
    <h2 class="contact-anim">Kontakt mig</h2>
    <div class="links-container">
      <a class="contact-anim" href="mailto:Ida.skjodt@gmail.com"
        >Ida.skjodt@gmail.com</a>
      <a class="contact-anim" href="tel:+4540238003">+45 40 23 80 03</a>
      <a class="linkedin-logo" href="https://www.linkedin.com/in/ida-so/" target="blank">
      <img src="../static/images/skills-icons/linkedin-icon.png" alt="linkedin">
      </a>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Contact',
  mounted: function () {
    this.$gsap.from('.contact-anim', {
      scrollTrigger: '#contact',
      opacity: 0,
      y: 30,
      duration: 0.3,
      stagger: 0.3,
      ease: 'power1.inOut',
    })
  },
}
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  background-color: #a093f0;
  padding: 72px 48px;
  text-align: center;

  h2 {
    text-transform: uppercase;
    color: white;
    font-size: 32px;
    padding-bottom: 32px;
    position: relative;
    text-transform: uppercase;
    &::after {
      content: '';
      position: absolute;
      width: 50%;
      height: 5px;
      background-color: #fff;
      left: 50%;
      bottom: 0;
      transform: translate(-50%, -50%);
    }
  }
}
.links-container {
  margin-top: 48px;
  display: flex;
  flex-direction: column;
  align-items: center;
  .linkedin-logo {
    width: 40px;
  }
  a {
    color: white;
    font-size: 20px;
    padding: 8px 0;
  }
}
@media only screen and (min-width: 1024px) {
  section {
    width: 100%;
    padding: 108px 64px;

    h2 {
      font-size: 32px;
      padding-bottom: 14px;
      &::after {
        width: 10%;
      }
    }
  }
  .links-container {
    margin-top: 24px;

    a {
      font-size: 18px;
      padding: 16px 0;
    }
  }
}

@media only screen and (min-width: 1440px) {
}
</style>
