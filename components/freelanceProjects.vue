<template>
  <section id="freelance">
    <div class="grid-conainer">
      <div class="side-box-container">
        <SideHeading title="Freelance Projekter" />
      </div>
      <div class="freelance-box freelance-anim">
        <h2>Country Wellness ApS</h2>
        <h3>September 2020 – Nuværende</h3>
        <span>
          Skabelse af visuel brand identitet. 
          Grafiske og digitale elementer såsom: logo, video, fotografi, til sociale medier.
        </span>
      </div>
      <div class="freelance-box freelance-anim">
        <h2>Smokepins ApS</h2>
        <h3>August 2020 – September 2020</h3>
        <span>
          Arbejdet videre med etablering af visuel identitet, samt grafisk designs og 
          illustrationer til hjemmeside.
        </span>
      </div>
      <div class="freelance-box freelance-anim">
        <h2>Naturrum Sønder Omme</h2>
        <h3>2016 – 2019</h3>
        <span>
          Skabelse af visuel brand identitet. Grafiske og digitale elementer såsom: 
          logo, video, fotografi, til sociale medier.
        </span>
      </div>
    </div>
  </section>
</template>

<script>
import SideHeading from '../components/sideHeadingBox.vue'

export default {
  name: 'FreelanceProjects',
  components: {
    SideHeading,
  },
  mounted: function () {
    this.$gsap.from('.freelance-anim', {
      scrollTrigger: {
        trigger: '#freelance',
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
.freelance-box {
  background-color: #e54575;
  padding: 24px;
  text-align: left;
  color: white;
  h2 {
    font-size: 26px;
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
  section {
    margin: 36px 0;
  }
  .freelance-box {
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
    grid-row: 1/4;
  }
}
</style>
