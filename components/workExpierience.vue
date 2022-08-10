<template>
  <section id="work-expierience">
    <div class="grid-conainer">
      <div class="side-box-container">
        <SideHeading title="Arbejdserfaring" />
      </div>
      <div class="work-expierience-box work-expierience-anim">
        <h2>BILLIG ANIMATION</h2>
        <h3>Digital Designer</h3>
        <span>August 2021 - September 2021</span>
        <ul>
          <li>
            Udarbejdelse af animationsfilm og explainer videoer i Vyond og After Effects, 
            samt redigering i Premiere Pro.  
            Samt udarbejdelse af illustrationer og grafikker i Illustrator og Photoshop.
          </li>
          <li>
            Kommunikation og samarbejde med kunder og kollegaer før/under/efter produktudvikling.
          </li>
          <li>
            Kreativ visuel formidling og idéudvikling af budskab til storyline og manuskript.
          </li>
        </ul>
      </div>
      <div class="work-expierience-box work-expierience-anim">
        <h2>BILLIG ANIMATION / VIRAL FILM</h2>
        <h3>Motion Graphics praktikant</h3>
        <span>Januar 2021 - April 2021</span>
        <ul>
          <li>
            Assisterende hjælper på filmsettet med teknisk udstyr, og produkt shoots set ups.
          </li>
          <li>
            Udarbejdelse af animationsfilm og explainer videoer i Vyond og After Effects, 
            samt redigering i Premiere Pro. 
            Samt udarbejdelse af illustrationer og grafikker i Illustrator og Photoshop.
          </li>
          <li>
            Kommunikation og samarbejde med kunder og kollegaer før/under/efter produktudvikling.
          </li>
          <li>
            Kreativ visuel formidling og idéudvikling af budskab til storyline og manuskript.
          </li>
        </ul>
      </div>
      <div class="work-expierience-box work-expierience-anim">
        <h2>BILLUND LUFTHAVN</h2>
        <h3>Kasseassistent i Sales</h3>
        <span>Maj 2019 - September 2021</span>
        <ul>
          <li>
            Holde overblik i pressede og travle situationer, samt levere tilfredstillende kundeservice.
          </li>
          <li>
            Kommunikation og tilstedeværelse  i et internationalt miljø.
          </li>
          <li>
            Kendskab til sikkerheds reglementer, og ansvarlighed heromkring.
          </li>
        </ul>
      </div>

      <div class="work-expierience-box work-expierience-anim">
        <h2>MENY SØNDER OMME</h2>
        <h3>Service medarbejder</h3>
        <span>Juni 2014 - August 2021</span>
        <ul>
          <li>
            Lukkeansvarlig: håndring og udførsel af diverse daglige opgaver med ordentlighed.
          </li>
          <li>
            Kurser/workshops med henblik på god kundekontakt og fokus på salg og mersalg.
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
      font-weight: 500;
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
    grid-row: 1/5;
  }
  .work-expierience-box {
    height: 100%;
  }
}
</style>
