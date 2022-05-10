<template>
  <div>
    <Header />
    <div id="spacer"></div>
    <TextBox text="Country Wellness" />
    <section class="project-details">
      <div>
        <h2 class="">PROJEKT BESKRIVELSE</h2>
        <p>
          Country Wellness er en lille skønhedssalon som ligger ude på landet i skønne omgivelser, 
          heraf navnet. Virksomheden er drevet af Birte som åbnede i 2020.
          Country Wellness tilbyder på nuværende tidspunkt fodbehandlinger og gellack negle. 
          Men har planer om at uddvide med blandt andet vipper.
          <br><br>
          Jeg har tæt kontakt med kunden siden opstart, og vi holder vores samarbejde kørende.
          Formålet med projektet var først at skulle etablere et visuelt udtryk af branded, 
          hvorefter kundens ønske var at oprette en Facebook side, for at kunne interagere med kunder.
          <br><br>
          Fremtidsplanerne for projektet at kunne skabe mere engagerende indhold, samt at oprette en
          tilhørende Instagram. På længere sigt når virksomheden vækster, vil en hjemmeside med et 
          booking system være relevant.
        </p>
      </div>
      <div>
        <img
          src="../static/images/country_wellness/country-wellness-business-card-mockup2.png"
          alt="Country Wellness business card mockup"
        />
      </div>
    </section>
    <ProjectDetails
      client="Country Wellness"
      :services="[
        'Rebranding',
        'Logo',
        'Grafisk design',
        'Sociale Medier',
      ]"
      :toolsSrc="[
        {
          src: require('../static/images/skills-icons/file-icons_adobe-photoshop.png'),
        },
        {
          src: require('../static/images/skills-icons/file-icons_adobe-premiere.png'),
        },
        {
          src: require('../static/images/skills-icons/file-icons_adobe-aftereffects.png'),
        },
        {
          src: require('../static/images/skills-icons/facebook-icon.png'), 
        },
        {
          src: require('../static/images/skills-icons/instagram-icon.png'), 
        },
      ]"
    />

    <TwoRowsLayout_cw headingText="Design" />
  </div>
</template>
<script>
import TextBox from '../components/textBox.vue'
import ProjectDetails from '../components/projectDetails.vue'
import TwoRowsLayout_cw from '../components/project_pages_components/PP_2_rows_cw.vue'
import Header from '~/components/header.vue'

export default {
  name: 'CountryWellness',
  components: {
    TextBox,
    ProjectDetails,
    TwoRowsLayout_cw,
    Header,
  },
  mounted() {
    window.scrollTo(0, 0)
  },
}
</script>

<style lang="scss" scoped>
#spacer {
  width: 100%;
  height: 8vh;
}

section.project-details {
  width: 100%;
  & > div:nth-of-type(1) {
    background-color: #f1ebe7;
    padding: 32px;
  }
  & > div:nth-of-type(2) {
    img {
      width: 100%;
    }
  }
  h2 {
    text-transform: uppercase;
    color: #95867d;
    font-size: 32px;
    padding-bottom: 32px;
    margin-bottom: 32px;
    position: relative;
    text-transform: uppercase;
    &::after {
      content: '';
      position: absolute;
      width: 50%;
      height: 5px;
      background-color: #95867d;
      left: 50%;
      bottom: 0;
      transform: translate(-50%, -50%);
    }
  }
  p {
    color: #95867d;
    font-size: 18px;
  }
}
@media only screen and (min-width: 1024px) {
  #spacer {
    height: 9vh;
  }
  section.project-details {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 36px;

    & > div:nth-of-type(1) {
      padding: 64px;
    }
    & > div:nth-of-type(2) {
      img {
        width: 100%;
        height: 100%;
        object-fit: cover;
      }
    }
    h2 {
      font-size: 32px;
      padding-bottom: 14px;
      margin-bottom: 24px;

      text-align: left;
      &::after {
        width: 10%;
        left: 0;
        transform: translateX(0);
      }
    }
    p {
      font-size: 18px;
      text-align: left;
    }
  }
}
</style>
