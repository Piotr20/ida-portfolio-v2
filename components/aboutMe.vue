<template>
  <section id="about-me">
    <div class="grid-container">
      <div class="text-wrapper">
        <h2 class="about-me-anim">IDA SKJØDT OLESEN</h2>
        <p class="about-me-anim">
          Jeg er særlig passioneret omkring at skabe fortællinger og dele
          budskaber gennem billeder og video, heriblandt særligt
          <strong>animation og motion graphics</strong>. Processen med at
          nørkler med små elementer, som forener sig og går ubemærket hen og
          bliver stykket sammen som en helhed, giver mig drive.

          <br /><br />
          For mig er arbejdsmiljøet med mine kollegaer en betydelig del af min
          motivation for mit arbejde, da det at <strong>samarbejder</strong> kan
          bibringe ellers usete perspektiver på en given sag. Jeg holder af at
          <strong>sprede godt humør</strong> blandt de mennesker jeg omgås
          dagligt.
        </p>
        <div class="based-in-aarhus">
          <img
            src="../static/images/based_in_aarhus_icon.png"
            alt="personal contact icon"
          />
          <h3>Aarhus</h3>
        </div>
      </div>
      <div class="image-wrapper">
        <img
          src="../static/images/holding_camera_filter.png"
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
    grid-template-columns: repeat(2, 1fr);
    grid-template-rows: repeat(3, 1fr);
    grid-gap: 36px;
    padding: 36px 0;
  }
  .text-wrapper {
    grid-column: 1/2;
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
    grid-column: 2/3;
    grid-row: 1/4;

    img {
      width: 100%;
      object-fit: cover;
      object-position: center 8%;
    }
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
