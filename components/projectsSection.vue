<template>
  <section>
    <div class="grid-container">
      <div class="project project-4">
        <div class="background-container"></div>
        <div class="content-contaienr">
          <h2 class="project-4-anim">Country Wellness</h2>
          <p class="project-4-anim">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc nisl
            enim pellentesque sodales id. Donec convallis maecenas viverra
            venenatis tincidunt consectetur pulvinar dignissim. Elit lacus donec
            at auctor commodo, urna auctor quam. Dolor consequat, eget elementum
            lacinia eleifend.
          </p>
          <NuxtLink class="project-4-anim" to="/">Se mere</NuxtLink>
        </div>
      </div>
      <div class="project project-2">
        <div class="background-container"></div>
        <div class="content-contaienr">
          <h2 class="project-2-anim">Smokepins</h2>
          <p class="project-2-anim">
            Gruppe eksamensprojekt med Smokepins som kunde. Projektet havde
            rigtig stor succes, i den forstand at kunden efterfulgt har
            implementeret store dele af websitet vi har udarbejdet, samt
            grafikker og markedsførings ideer. En kæmpe fornøjelse at samarbejde
            med en kunde og se reelt brugbare resultater.
          </p>
          <NuxtLink class="project-2-anim" to="/Smokepins">Se mere</NuxtLink>
        </div>
      </div>
      <div class="project project-3">
        <div class="background-container"></div>
        <div class="content-contaienr">
          <h2 class="project-3-anim">ReGrow</h2>
          <p class="project-3-anim">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc nisl
            enim pellentesque sodales id. Donec convallis maecenas viverra
            venenatis tincidunt consectetur pulvinar dignissim. Elit lacus donec
            at auctor commodo, urna auctor quam. Dolor consequat, eget elementum
            lacinia eleifend.
          </p>
          <NuxtLink class="project-3-anim" to="/Regrow">Se mere</NuxtLink>
        </div>
      </div>

      <!-- OTHER PROJECTS -->

      <!--  <div class="project project-1">
        <div class="background-container"></div>
        <div class="content-contaienr">
          <h2 class="project-1-anim">Billig Animation</h2>
          <p class="project-1-anim">
            Aflsuttende eksamensprojekt med Billig Animation som kunde. Et
            projekt der nytænkede den måde firmaet brandede sig på, og skabte en
            ny sjov visuel fremtoning. Projektet var meget alsidigt og mange
            forskellige værktøjer blev benyttet.
          </p>
          <router-link class="project-1-anim" to="/billiganimation"
            >Se mere</router-link
          >
        </div>
      </div> -->
      <!-- <div class="project project-5">
        <div class="background-container"></div>
        <div class="content-contaienr">
          <h2 class="project-5-anim">Projekt</h2>
          <p class="project-5-anim">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc nisl
            enim pellentesque sodales id. Donec convallis maecenas viverra
            venenatis tincidunt consectetur pulvinar dignissim. Elit lacus donec
            at auctor commodo, urna auctor quam. Dolor consequat, eget elementum
            lacinia eleifend.
          </p>
          <router-link class="project-5-anim" to="/">Se mere</router-link>
        </div>
      </div> -->
    </div>
  </section>
</template>

<script>
// import { gsap } from 'gsap'
// import { ScrollTrigger } from 'gsap/ScrollTrigger'

// gsap.registerPlugin(ScrollTrigger)
export default {
  name: 'ProjectsSection',
  // methods: {
  //   call() {
  //     window.pageY = 0;
  //   },
  // },
  mounted: function () {
    // gsap.from('.project-1-anim', {
    //   scrollTrigger: {
    //     trigger: '.project-1',
    //     start: 'top 70%',
    //   },
    //   opacity: 0,
    //   y: 30,
    //   duration: 0.3,
    //   stagger: 0.3,
    //   ease: 'power1.inOut',
    // })
    // gsap.from('.project-2-anim', {
    //   scrollTrigger: {
    //     trigger: '.project-2',
    //     start: 'top 70%',
    //   },
    //   opacity: 0,
    //   y: 30,
    //   duration: 0.3,
    //   stagger: 0.3,
    //   ease: 'power1.inOut',
    // })
    // gsap.from('.project-3-anim', {
    //   scrollTrigger: {
    //     trigger: '.project-3',
    //     start: 'top 70%',
    //   },
    //   opacity: 0,
    //   y: 30,
    //   duration: 0.3,
    //   stagger: 0.3,
    //   ease: 'power1.inOut',
    // })
    // gsap.from('.project-4-anim', {
    //   scrollTrigger: {
    //     trigger: '.project-4',
    //     start: 'top 70%',
    //   },
    //   opacity: 0,
    //   y: 30,
    //   duration: 0.3,
    //   stagger: 0.3,
    //   ease: 'power1.inOut',
    // })
    // gsap.from('.project-5-anim', {
    //   scrollTrigger: {
    //     trigger: '.project-5',
    //     start: 'top 70%',
    //   },
    //   opacity: 0,
    //   y: 30,
    //   duration: 0.3,
    //   stagger: 0.3,
    //   ease: 'power1.inOut',
    // })
  },
}
</script>

<style lang="scss" scoped>
section {
  width: 100%;
}
.grid-container {
  width: 100%;
  grid-auto-rows: minmax(min-content, max-content);
  display: grid;
  grid-gap: 24px;
}
.project {
  width: 100%;
  height: 100%;
  position: relative;
  cursor: pointer;
  .background-container {
    position: absolute;
    width: 100%;
    height: 100%;
    opacity: 0;
    transition: opacity 0.3s ease;
    background-position: center;
    z-index: 1;
  }
  &:nth-of-type(1) .background-container {
    background-image: url('../static/images/billig_animation/business_card_mockup_billiganimation.png');
    background-repeat: no-repeat;
    background-size: cover;
  }
  &:nth-of-type(2) .background-container {
    background-image: url('../static/images/smokepins/Business_Card_Mockup_Smokepins.png');
    background-repeat: no-repeat;
    background-size: cover;
  }
  &:nth-of-type(3) .background-container {
    background-image: url('../static/images/regrow/regrow_business_card_mockup2.png');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;
  }
  &:hover .background-container {
    opacity: 0.4;
  }
  .content-contaienr {
    position: relative;
    width: 100%;
    color: white;
    padding: 32px;
    display: flex;
    flex-direction: column;
    z-index: 3;
    h2 {
      font-size: 32px;
      padding-bottom: 12px;
      position: relative;
      text-transform: uppercase;
      text-align: left;
      &::after {
        content: '';
        position: absolute;
        width: 40%;
        height: 5px;
        background-color: #fff;
        left: 0;
        bottom: 0;
      }
    }
    p {
      padding-top: 32px;
      font-size: 18px;
      text-align: left;
    }
    a {
      display: inline-block;
      align-self: flex-start;
      margin-top: 24px;
      background-color: #fff;
      text-decoration: none;
      padding: 8px 32px 8px 12px;
      text-transform: uppercase;
      border: 2px solid white;
      transition: all 0.3s ease;
      font-weight: 600;
      &:hover {
        background-color: transparent;
        color: white;
      }
    }
  }
}
.project-1,
.project-4 {
  background-color: #e877c1;
  a {
    color: #e877c1;
  }
}
.project-2,
.project-5 {
  background-color: #b6abf9;
  a {
    color: #b6abf9;
  }
}

.project-3 {
  background-color: #e54575;
  a {
    color: #e54575;
  }
}

@media only screen and (min-width: 1024px) {
  section {
    width: 100%;
  }
  .grid-container {
    grid-template-columns: repeat(2, 1fr);
    grid-auto-rows: minmax(min-content, max-content);
    grid-gap: 36px;
  }
  .project {
    .content-contaienr {
      padding: 64px;
      display: flex;
      flex-direction: column;
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
      p {
        padding-top: 24px;
        font-size: 18px;
        width: 85%;
      }
      a {
        align-self: flex-start;
        margin-top: 24px;
        padding: 6px 24px 6px 8px;
        border-width: 3px;
        font-size: 16px;
      }
    }
  }
  .project-3 {
    grid-row: 2/3;
    grid-column: 1/3;
    .content-contaienr {
      h2 {
        text-align: center;
        &::after {
          left: 50%;
          transform: translateX(-50%);
          width: 10%;
        }
      }
      p {
        width: 50%;
        margin: 0 auto;
        text-align: center;
      }
      a {
        margin-left: auto;
        margin-right: auto;
        padding: 6px 16px;
      }
    }
  }
}
@media only screen and (min-width: 1440px) {
  .project {
    p {
      font-size: 22px;
    }
  }
}
</style>
