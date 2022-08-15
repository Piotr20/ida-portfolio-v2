<template>
  <section id="about-me">
    <div class="grid-container">
      <div class="text-wrapper">
        <h2 class="about-me-anim">IDA SKJØDT OLESEN</h2>
        <p class="about-me-anim">
          Hej jeg hedder Ida, jeg er 23 år og er bosat i Højbjerg, Aarhus. 
          Jeg er uddannet <strong>Multimediedesigner</strong> og har tidligere beskæftiget mig med animation. 
          <br/><br/>
          Jeg er særlig passioneret omkring at skabe fortællinger og dele
          budskaber gennem billeder og video, heriblandt særligt
          <strong>animation og motion graphics</strong>. Det giver mig et kæmpe drive
          hele processen med at arbejde på små detajler som forener sig og
          bliver stykket sammen til en helhed.
          <br/><br/>
          For mig er arbejdsmiljøet med mine kollegaer en betydelig del af min
          motivation for mit arbejde, da det at <strong>samarbejde</strong> kan
          bibringe ellers usete perspektiver. Jeg holder af at sprede godt humør 
          blandt mine medmennesker.
        </p>
        <h3 class="about-me-anim">Hvem er jeg så?</h3>
        <p class="about-me-anim">
          Jeg er rigtig glad for at være aktiv, og træner i fitness samt dyrker fodbold, 
          Det hænder også jeg sidder foran fjerneren og ser bold.
          Derudover holder jeg meget af at vandre, hvortil min seneste tur var 
          bjergvandring i det sydlige Polen.
          Jeg er frivillig indsamler ved 'Gå for BørneTelefonen', og i den forbindelse skal jeg til Spanien 
          og vandre den Engelske Camino i september. 
          <br/><br/>
          <span>Fun Fact: Jeg er en kæmpe dyreelsker med slem pelsdyr allergi.</span>
          
        </p>
        <!-- <div class="based-in-aarhus about-me-anim">
          <img
            src="../static/images/based_in_aarhus_icon.png"
            alt="personal contact icon"
          />
          <h3>Aarhus</h3>
        </div> -->
      </div>
      <div class="image-wrapper">
        <!-- ----------------- SLIDESHOW -----------------
        <ul id="slideWrap"> 
          <li><img src="../static/images/ida-holding_camera.png" alt=""></li>
          <li><img src="../static/images/ida-heste.JPG" alt=""></li>
          <li><img src="../static/images/ida-vandre.JPG" alt=""></li>
          <li><img src="../static/images/ida_atv.jpg" alt=""></li>
        </ul> -->
        <img
          src="../static/images/ida-holding_camera.png"
          alt="Ida's image"
        />
      </div>
      
    </div>
  </section>
</template>

<script>
export default {
  name: 'AboutMe',
  mounted: function () {
    this.$gsap.from('.about-me-anim', {
      scrollTrigger: {
        trigger: '#about-me',
        start: 'top 70%',
      },
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
}
.grid-container {
  width: 100%;
  grid-gap: 24px;
  padding: 24px 0;
}
.image-wrapper {
  height: 100%;
  display: flex;
  overflow: hidden;
  position: relative;
  &::after {
    content: '';
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    position: absolute;
    z-index: 1;
    opacity: 0.4;
  }
  &:nth-of-type(2),
  &:nth-of-type(2)::after {
    background-color: #eb78c4;
  }
  &:nth-of-type(3),
  &:nth-of-type(3)::after {
    background-color: #b6abf9;
  }
  &:nth-of-type(4),
  &:nth-of-type(4)::after {
    background-color: #e54575;
  }
  img {
    height: 100%;
    width: 100%;
    object-fit: cover;
    object-position: center 10%;
  }
  div {
    width: 25%;
    color: white;
    font-size: 64px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}

.text-wrapper {
  background-color: #f1ebe7;
  color: #95867d;
  padding: 32px;
  h2 {
    font-size: 32px;
    padding-bottom: 32px;
    position: relative;
    text-align: left;
    &::after {
      content: '';
      position: absolute;
      width: 40%;
      height: 5px;
      background-color: #95867d;
      left: 0;
      bottom: 0;
    }
  }
  p {
    padding-top: 32px;
    font-size: 18px;
    text-align: left;
    span {
      font-style: italic;
  }
  }
}
.based-in-aarhus {
  display: flex;
  align-items: center;
  padding-top: 32px;
  img {
    width: 75px;
  }
  h3 {
    padding-left: 16px;
    font-size: 22px;
  }
}
@media only screen and (min-width: 1024px) {
  .grid-container {
    display: grid;
    grid-template-columns: repeat(3, 2fr);
    grid-template-rows: repeat(3, 1fr);
    grid-gap: 36px;
    padding: 36px 0;
  }
  .text-wrapper {
    grid-column: 1/3;
    grid-row: 1/4;
    padding: 64px;
    h2 {
      font-size: 32px;
      text-align: left;
      &::after {
        left: 0;
        transform: translateX(0);
        width: 15%;
      }
      padding-bottom: 14px;
    }
    h3 {
      padding-top: 50px;
      font-size: 26px;
      font-weight: 500;
      text-align: left;
      
    }
    p {
      padding-top: 20px;
      font-size: 18px;
      width: 85%;
    }
  }
  .image-wrapper {
    width: 100%;
    display: flex;
    overflow: hidden;
    height: 100%;
    grid-column: 3/3;
    grid-row: 1/4;
    img {
      width: 100%;
      object-fit: cover;
      object-position: center 8%;
    }
    /* ----------------- SLIDESHOW -----------------
    ul {
      position: relative;
      list-style: none;
      height: 100%;
      width: 10000%;
      padding: 0;
      margin: 0;
      transition: all 750ms ease;
      left: 0;
    }
    ul li {
      position: relative;
      height: 100%;
      float: left;
    } 
    */
  }
  .based-in-aarhus {
    padding-top: 64px;
    img {
      width: 90px;
    }
    h3 {
      font-size: 24px;
    }
  }
}
</style>
