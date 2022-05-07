<template>
  <div>
    <Header />
    <div id="spacer"></div>
    <TextBox text="regrow" />
    <section class="project-details">
      <div>
        <h2 class="">PROJEKT BESKRIVELSE</h2>
        <p>
          RePot er dansk startup virksomhed skabt af tre studerende fra Digital
          Konceptudvikling på Erhvervsakademi Aarhus. Målet for virksomheden er
          at sælge 100% bionedbrydelige potter, samt at skabe opmærksomhed
          omkring bæredygtig udvikling og oprette et community omkring dette.
          <br /><br />
          Projektet havde til formål at skabe et solidt fundament for
          virksomhedens fremtid gennem ’Storyscaping’ konceptet. Dette indebærer
          at kreere et univers med fordybende oplevelser som kan skabe en
          relation mellem brandet og kunden, som giver emotionel engageret
          kunder som afkast.
        </p>
      </div>
      <div>
        <img
          src="../static/images/regrow/regrow_business_card_mockup2.png"
          alt="Regrow business card mockup"
        />
      </div>
    </section>
    <ProjectDetails
      client="RePot ApS"
      :services="[
        'Rebranding',
        'Logo',
        'Website',
        'Storyscaping - UX',
        'Animations',
        'Social Media',
      ]"
      :toolsSrc="[
        {
          src: require('../static/images/skills-icons/file-icons_adobe-photoshop.png'),
        },
        {
          src: require('../static/images/skills-icons/file-icons_adobe-illustrator.png'),
        },

        {
          src: require('../static/images/skills-icons/file-icons_adobe-premiere.png'),
        },

        {
          src: require('../static/images/skills-icons/file-icons_adobe-aftereffects.png'),
        },
        {
          src: require('../static/images/skills-icons/file-icons_adobe-xd.png'),
        },
        {
          src: require('../static/images/skills-icons/akar-icons_html-fill.png'),
        },
        {
          src: require('../static/images/skills-icons/akar-icons_css-fill.png'),
        },
        {
          src: require('../static/images/skills-icons/brandico_wordpress.png'),
        },
      ]"
    />

    <TwoRowsLayout_regrow />
  </div>
</template>
<script>
import TextBox from '../components/textBox.vue'
import ProjectDetails from '../components/projectDetails.vue'
import TwoRowsLayout_regrow from '../components/project_pages_components/PP_2_rows_regrow.vue'

export default {
  components: {
    TextBox,
    ProjectDetails,
    TwoRowsLayout_regrow,
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
    height: 12vh;
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
