<template>
  <section id="technical-skills">
    <h2 class="technical-skills-anim">TEKNISK ERFARING</h2>
    <div class="wrapper">
      <!-- Desktop headings -->
      <div class="skills-text technical-skills-anim">
        <h3 class="technical-skills-anim">Advanced</h3>
      </div>
      <div class="skills-text technical-skills-anim">
        <h3 class="technical-skills-anim">Intermediate</h3>
      </div>
      <div class="skills-text technical-skills-anim">
        <h3 class="technical-skills-anim">Basic</h3>
      </div>
      
      <!-- Mobile heading -->
      <div class="skills-text-mobile technical-skills-anim">
        <h3 class="technical-skills-anim">Advanced</h3>
      </div>

      <!-- Bruger -->
      <div class="skills-container">
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/file-icons_adobe-photoshop.png"
            alt=""
          />
        </div>
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/file-icons_adobe-premiere.png"
            alt=""
          />
        </div>
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/file-icons_adobe-aftereffects.png"
            alt=""
          />
        </div>
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/file-icons_adobe-xd.png"
            alt=""
          />
        </div>
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/mdi_microsoft-office.png"
            alt=""
          />
        </div>
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/vyond_Logo.png"
            alt=""
          />
        </div>
      </div>

      <!-- Mobile heading -->
      <div class="skills-text-mobile technical-skills-anim">
        <h3 class="technical-skills-anim">Intermediate</h3>
      </div>

      <!-- Advanceret -->
      <div class="skills-container">
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/file-icons_adobe-illustrator.png"
            alt=""
          />
        </div>
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/akar-icons_html-fill.png"
            alt=""
          />
        </div>
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/akar-icons_css-fill.png"
            alt=""
          />
        </div>
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/figma-logo.png"
            alt=""
          />
        </div>
      </div>

      <!-- Mobile heading -->
      <div class="skills-text-mobile technical-skills-anim">
              <h3 class="technical-skills-anim">Basic</h3>
            </div>

      <!-- Ekspert -->
      <div class="skills-container">
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/brandico_wordpress.png"
            alt=""
          />
        </div>
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/elementor-logo.png"
            alt=""
          />
        </div>
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/invision-logo.png"
            alt=""
          />
        </div>
        <div class="icon-box">
          <img
            class="technical-skills-anim"
            src="../static/images/skills-icons/monday-logo-new.png"
            alt=""
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'TechnicalSkills',
  mounted: function () {
    this.$gsap.from('.technical-skills-anim', {
      scrollTrigger: {
        trigger: '#technical-skills',
        start: 'top 70%',
      },
      opacity: 0,
      y: 30,
      duration: 0.3,
      stagger: 0.15,
      ease: 'power1.inOut',
    })
  },
}
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  background-color: #e877c1;
  padding: 32px;
  h2 {
    text-align: center;
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
.wrapper {
  margin-top: 50px;
  display: grid;
  width: 100%;
  height: auto;
  grid-template-columns: repeat(1, 1fr);
  grid-template-rows: repeat(3, 50px 2fr);
}
.skills-text{
  display: none;
}
h3 {
    color: white;
    font-size: 22px;
    text-align: center;
  }
.skills-container {
  padding: 25px 18px;
  background-color: rgba(255, 255, 255, 0.3);
  display: grid;
  width: 100%;
  margin-bottom: 50px;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: minmax(min-content, max-content);
  grid-gap: 20px;
  .icon-box {
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    img {
      width: 80%;
    }
  }
  .vyond-logo {
    grid-column: 1/3;
     img {
      width: 60%;
    }
  }
  .monday-logo {
     grid-column: 3/5;
   img {
      width: 110%;
    }
  }
}
@media only screen and (min-width: 1024px) {
  section {
    width: 100%;
    padding: 64px;
    padding-bottom: 80px;
    h2 {
      font-size: 32px;
      padding-bottom: 20px;
      &::after {
        width: 10%;
      }
    }
  }
h3 {
    color: white;
    font-size: 25px;
    text-align: center;
  }
.skills-text-mobile{
  display: none;
}
.skills-text{
  display: block;
}
.wrapper {
    display: grid;
    padding-top: 50px;
    align-items: center;
    margin: 0 auto;
    width: 90%;
    height: auto;
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(1, 1fr 2fr);
    
  }
  .skills-container {
    grid-template-columns: repeat(3, 1fr);
    grid-template-rows: repeat(2, 1fr);
    padding: 30px 30px;
    width: 85%;
    margin: 0 auto;
    justify-items: center;
    align-items: center;
    .icon-box {
      width: 100%;
      img {
      width: 90%;
    }
    }
    .vyond-logo {
      grid-column: 1/4;
      img {
      width: 50%;
    }
    }
    .monday-logo {
      width: 80%;
      grid-column: 4/7;
      grid-row: 3/4;
      justify-self: center;
    }
  }
}
</style>
