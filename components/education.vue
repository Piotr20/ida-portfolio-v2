<template>
  <section id="education">
    <div class="grid-conainer">
      <div class="side-box-container">
        <SideHeading title="Uddannelse" />
      </div>
      <div class="education-box education-anim">
        <h2>Business Academy Aarhus</h2>
        <h3>2019 - 2021</h3>
        <span>Multimedia Design AP - Content Creation</span>

        <ul>
          <li>
            Gennem uddannelsen har jeg udvidet min faglighed indenfor
            grundlæggende design teori, herunder digital design og lært omkring
            psykologiske faktorer der påvirker brugere. Jeg har kunne
            implementere denne viden i virkelighedsnære projekter.
          </li>
          <li>
            Jeg har lært om traditionel markedsføring samt markedsføring gennem
            sociale medier og om hvordan man henvender sig strategisk til
            målgruppen, med målrettet content.
          </li>
          <li>
            Jeg har arbejdet med forskellige content typer, herunder grafiske
            elementer, video og animation (motion graphics) henvendt til
            specifikke målgrupper.
          </li>
          <li>
            Jeg har arbejdet med frontend programmering af hjemmesider, samt
            arbejdet med CMS-systemer.
          </li>
          <li>
            I projekter har jeg primært stået for organiseringen og planlægning
            af arbejdsforløbet. Jeg har sørget for at alle opgaver bliver lavet
            i følge tidsplanen, og haft det forkromende overblik hele vejen
            igennem.
          </li>
          <li>
            Gennem den internationale linje har jeg udviklet mine internationale
            og sproglige kompetencer, herunder fået en global forståelse af
            kulturer.
          </li>
        </ul>
      </div>

      <div class="education-box education-anim">
        <h2>Erhvervsgymnasiet Grindsted</h2>
        <h3>2015 - 2018</h3>
        <span
          >Højere Teknisk Eksamen (HTX) - Kommunikation & IT <br /><br />Uddrag
          fra udtalelsen til legatmodtagelse:
        </span>
        <ul>
          <li>
            Legatmodtageren har altid stillet sig til rådighed for skolen.
          </li>
          <li>
            Legatmodtageren har igennem sine år på skolen påtaget sig et ansvar
            for alles trivsel.
          </li>
          <li>Legatmodtageren tager ansvar for egen læring og udvikling.</li>
          <li>
            Legatmodtageren har haft overskud til at deltage i skolerelateret
            aktiviteter udenfor skoletiden.
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
    // gsap.from(".education-anim", {
    //   scrollTrigger: {
    //     trigger: "#education",
    //     start: "top 70%",
    //   },
    //   opacity: 0,
    //   y: 30,
    //   duration: 0.3,
    //   stagger: 0.3,
    //   ease: "power1.inOut",
    // });
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
