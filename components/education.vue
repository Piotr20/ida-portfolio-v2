<template>
  <section id="education">
    <div class="grid-conainer">
      <div class="side-box-container">
        <SideHeading title="Uddannelse" />
      </div>
      <div class="education-box education-anim">
        <h2>Multimedia Design AP - Business Academy Aarhus</h2>
        <h3>2019 - 2021</h3>
        <span>Specialisering: Content Creation</span>

        <ul>
          <li>
            Praktisk viden omkring kreative design processer og teorier. 
            Erfaring med forskellige content typer, såsom: illustrationer, billeder, 
            video, animation og motion graphics, til hjemmeside og sociale medier.
          </li>
          <li>
            Social medie marketing og anvendelse af marketing og content strategier.
          </li>
          <li>
            Projekter (gruppe og individuel) der omhandler udvikling af løsninger og 
            produkter for reelle kunder. Arbejdet med frontend programmering og CMS-systemer.
          </li>
          <li>
            Internationale og sproglige kompetencer, herunder global forståelse af kulturer.
          </li>
        </ul>
      </div>

      <div class="education-box education-anim">
        <h2>Højere Teknisk Eksamen (HTX) - Erhvervsgymnasiet Grindsted</h2>
        <h3>2015 - 2018</h3>
        <span
          >Studieretning: Kommunikation & IT - Valgfag: Mediefag C
        </span>
        <ul>
          <li>
            Forskellige kommunikations projekter med reelle kunder, 
            omhandlende problem analysering og anvendelse af relevante metoder for produkt testning.
          </li>
          <li>
            Viden om design og kommunikations teorier og strategier for digital og printet platforme.
          </li>
          <li>Viden om forskellige genre, medie platforme og sammenspillet mellem. Forståelse for 
            fundamentale egenskaber ved fakta og fiktion, samt hvordan de supplere hinanden.
            </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
import SideHeading from '../components/sideHeadingBox.vue'

export default {
  name: 'Education',
  components: {
    SideHeading,
  },
  mounted: function () {
    this.$gsap.from('.education-anim', {
      scrollTrigger: {
        trigger: '#education',
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
.grid-conainer {
  display: grid;
  width: 100%;
  grid-auto-rows: minmax(min-content, max-content);
  grid-gap: 24px;
}
.education-box {
  background-color: #e877c1;
  padding: 24px;
  text-align: left;
  color: white;
  h2 {
    font-size: 26px;
    text-transform: uppercase;
  }
  h3 {
    font-size: 20px;
    padding-top: 8px;
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
  .grid-conainer {
    grid-template-columns: 2fr 1fr;
    grid-auto-rows: minmax(min-content, max-content);
    grid-gap: 36px;
    .education-box {
      padding: 48px;
    }
    h2 {
      font-size: 32px;
      font-weight: 500;
    }
    h3 {
      font-size: 22px;
      padding-top: 2px;
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
    grid-row: 1/3;
    grid-column: 2/3;
  }
}
</style>
