<template>
  <section id="work-expierience">
    <div class="grid-conainer">
      <div class="side-box-container">
        <SideHeading title="Arbejdserfaring" />
      </div>

      <div class="work-expierience-box work-expierience-anim">
        <h2>BILLUND LUFTHAVN</h2>
        <h3>Maj 2019 - September 2021</h3>
        <span>Kasseassistent i Sales</span>
        <ul>
          <li>
            At kunne holde et overblik i pressede situationer, samt at levere en
            god service til kunder, så de har en god oplevelse og en god start
            på deres rejse.
          </li>
          <li>
            At opholde sig i et internationalt miljø, at kommunikere blandt
            mange kulturer.
          </li>
          <li>
            At sikre sig at sikkerheds reglementer bliver overholdt, både for
            kunder og personalets sikkerhed.
          </li>
        </ul>
      </div>

      <div class="work-expierience-box work-expierience-anim">
        <h2>MENY SØNDER OMME</h2>
        <h3>Juni 2014 - August 2021</h3>
        <span>Service medarbejder</span>
        <ul>
          <li>
            Ansvarlig for at butikken i aftentimerne, samt at kunne håndtere og
            løse evt. uforudsete situationer der kunne opstå.
          </li>
          <li>
            Sørge for at kunderne får en god oplevelse på deres indkøbstur, og
            at de får den hjælp de har behov for, samt at de får et smil med på
            vejen.
          </li>
        </ul>
      </div>

      <div class="work-expierience-box work-expierience-anim">
        <h2>VIRAL FILM / BILLIG ANIMATION</h2>
        <h3>Januar 2021 - April 2021</h3>
        <span>Motion Graphics praktikant</span>
        <ul>
          <li>
            Jeg har gennem praktikken været en del af den overordnede
            arbejdsproces. Fra kunden kommer med et ønske om animationsfilm til
            de får deres færdige produkt.
          </li>
          <li>
            Kundekontakt i forbindelse med opstartsfasen, dialoger om hvilket
            produkt kunden ønsker. Samt sparring med kunden gennem hele fasen.
          </li>
          <li>
            Udarbejdelse af animationsfilm, i programmet Vyond, samt redigering
            og lyddesign af filmen i Premiere Pro.
          </li>
          <li>
            Udarbejdelse af grafikker, i Illustrator og photoshop, samt
            udarbejdelse af video og animation, i After Effects, som som
            supplement til animationsfilm.
          </li>
          <li>
            En stor del af arbejdet har involveret kreativ formidling af diverse
            budskaber skriftligt, visuelt og auditiv.
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
import SideHeading from '../components/sideHeadingBox.vue'

export default {
  name: 'WorkExpierience',
  components: {
    SideHeading,
  },
  mounted: function () {
    this.$gsap.from('.work-expierience-anim', {
      scrollTrigger: {
        trigger: '#work-expierience',
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
  margin: 24px 0;
}
.grid-conainer {
  display: grid;
  width: 100%;
  grid-auto-rows: minmax(min-content, max-content);
  grid-gap: 24px;
}
.work-expierience-box {
  background-color: #a093f0;
  padding: 24px;
  text-align: left;
  color: white;
  h2 {
    font-size: 26px;
  }
  h3 {
    font-size: 20px;
    padding-top: 2px;
    margin-bottom: 24px;
  }
  span {
    font-size: 18px;
  }
  ul {
    margin-top: 8px;
    padding-left: 16px;
    li {
      padding: 8px 0;
    }
  }
}
@media only screen and (min-width: 1024px) {
  section {
    margin: 36px 0;
  }
  .work-expierience-box {
    padding: 48px;
  }
  .grid-conainer {
    grid-template-columns: 1fr 2fr;
    grid-auto-rows: minmax(min-content, max-content);
    grid-gap: 36px;
    h2 {
      font-size: 32px;
    }
    h3 {
      font-size: 22px;
      margin-bottom: 8px;
    }
    span {
      font-size: 18px;
    }
    ul {
      margin-top: 8px;
      font-size: 18px;
      padding-left: 24px;
      li {
        padding: 8px 0;
        max-width: 75ch;
      }
    }
  }
  .side-box-container {
    grid-row: 1/4;
  }
  .work-expierience-box {
    height: 100%;
  }
}
</style>
