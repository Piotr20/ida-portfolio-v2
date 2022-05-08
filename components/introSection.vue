<template>
  <section id="home">
    <video src="../static/videos/video_intro.mp4" autoplay loop muted />
    <div class="viedo-overlay"></div>
    <div class="overlay">
      <h1 class="intro-anim">Halløj!</h1>
      <h2 class="intro-anim">
        Jeg er <strong>digital designer</strong> med interesse for
        <strong>motion graphic design</strong>
      </h2>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {}
  },
  name: 'IntroSection',
  props: {},
  mounted: function () {
    this.$gsap.from('.intro-anim', {
      scrollTrigger: '#home', // start the animation when ".box" enters the viewport (once)
      opacity: 0,
      y: 30,
      duration: 0.3,
      stagger: 0.3,
      ease: 'power1.inOut',
    })
  },
}
</script>

<style scoped lang="scss">
section {
  width: 100%;
  height: 100vh;
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: flex-end;
  video {
    width: 100%;
    height: 100%;
    padding-top: 8vh;
    object-fit: cover;
  }
  .viedo-overlay {
    position: absolute;
    z-index: 1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: #b5abf9;
    opacity: 0.7;
  }
  .overlay {
    position: absolute;
    z-index: 2;
    top: calc(45% + 8vh);
    transform: translateY(-50%);
  }
  & > * {
    color: white;
  }
  h1 {
    font-size: 112px;
    line-height: 130%;
    border-bottom: 8px solid white;
    padding-bottom: 8px;
    width: 85%;
    margin: 0 auto;
  }
  h2 {
    width: 85%;
    padding-top: 4px;
    font-size: 20px;
    margin: 0 auto;
    font-weight: normal;
  }
}

@media only screen and (min-width: 1024px) {
  section {
    .overlay {
      top: calc(50% + 9vh);
      transform: translateY(-50%);
    }
    video {
      padding-top: 9vh;
    }
    h1 {
      font-size: 288px;
      padding-bottom: 12px;
      width: auto;
      border-bottom: 16px solid white;
    }
    h2 {
      width: auto;
      font-size: 24px;
      margin-top: 18vh;
      margin-bottom: 10vh;
    }
  }
}
</style>
