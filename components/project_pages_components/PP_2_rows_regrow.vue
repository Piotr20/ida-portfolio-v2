<template>
  <section id="2-rows-grid">
    <h2 class="about-me-anim">Brandets budskab</h2>

    <div class="grid-container">
      <div class="cell-1">
        <p>
          RePot skal være et brand der har en meget direkte kommunikation, der er
          seriøs, dramatisk og kraftfuld. Skaberne bag RePot har udtalt at de ikke
          var blege for at være netop dette.
          <br /><br />
          Brandet er mere en ’bare’ et produkt, de er forgænger for at skabe
          opmærksomhed omkring bæredygtighed, det er et community, herved blev
          ReGrow til.
          <br /><br />
          ReGrow’s Organizing Idea er ”It is your time”, som illustrere at ’du’
          skal tage handling, det er ‘dig’ som har et valg. Brandet er
          opmærksomhed på at rede planeten, og med dette statement sætter det
          tiden i fokus, det er nu det skal ske. ReGrow fokusere på den større
          sag, det handler ikke kun om at sælge et produkt.
        </p>
      </div>

      <div class="cell-2">
        <video
          id="video-1"
          src="../../static/images/regrow/It_is_your_time_ver1.mp4"
          controls
          autoplay
          loop
        ></video>
      </div>

      <div class="cell-3">
        <h2 class="about-me-anim">Visuelt udtryk</h2>
        <img src="../../static/images/regrow/cards-mockups.png" alt="" />
        <br />
      </div>

      <div class="cell-4">
        <img
          src="../../static/images/regrow/styletile_regrow_ver2.png"
          alt="Styletile Regrow Ver 2"/>
      </div>

      <div class="cell-5">
        <h2 class="about-me-anim">Website</h2>
        <div class="mockups-wrapper">
          <img
            src="../../static/images/regrow/mockup-frontpage.png"
            alt="mockup frontpage"/>
          <img
            src="../../static/images/regrow/mockup-environment.png"
            alt="mockup environment"/>
          <img
            src="../../static/images/regrow/mockup-about.png"
            alt="mockup about us"/>
        </div>
      </div>

      <div class="cell-6"></div>
      <div class="cell-7"></div>
      <div class="cell-8"></div>
      <div class="cell-9"></div>
      <div class="cell-10"></div>
      <div class="cell-11"></div>
      <div class="cell-12"></div>
      <div class="cell-13"></div>
      <div class="cell-14"></div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'TwoRowsLayout_smokepins',
  props: {
    headingText: String,
  },
  methods: {
    playPauseVideo() {
      let videos = document.querySelectorAll('#video-1')
      videos.forEach((video) => {
        // We can only control playback without insteraction if video is mute
        video.muted = true
        // Play is a promise so we need to check we have it
        let playPromise = video.play()
        if (playPromise !== undefined) {
          playPromise.then((_) => {
            let observer = new IntersectionObserver(
              (entries) => {
                entries.forEach((entry) => {
                  if (entry.intersectionRatio !== 1 && !video.paused) {
                    video.pause()
                  } else if (video.paused) {
                    video.play()
                  }
                })
              },
              { threshold: 0.2 }
            )
            observer.observe(video)
          })
        }
      })
    },
  },
  mounted() {
    // And you would kick this off where appropriate with:
    this.playPauseVideo()
    this.$gsap.from('#video-1', {
      scrollTrigger: {
        trigger: '#video-1',
        start: 'top 70%',
      },
      opacity: 0,
      y: 30,
      duration: 0.3,
      stagger: 0.3,
      ease: 'power1.inOut',
      onEnter: ({ progress, direction, isActive }) => {
        console.log(progress, direction, isActive)
      },
    })
  },
}
</script>

<style lang="scss" scoped>
section {
  background-color: #f1ebe7;
  padding: 32px;
}
h2 {
  color: #95867d;
  text-transform: uppercase;
  font-size: 32px;
  padding-bottom: 32px;
  position: relative;

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
.grid-container {
  padding: 24px 0;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: 1fr 1fr;
  grid-gap: 24px;
  div {
    text-align: left;
    &:nth-of-type(2) {
      display: flex;
      justify-content: center;
      align-items: center;
    }
    &:nth-of-type(4) {
      display: flex;
      justify-content: center;
      align-items: center;
    } //the type is reffering to which grid box
    // 4th you dumbass :)
  }
  .cell-2 {
    video {
      width: 100%;
      height: 100%;
      object-fit: cover;
    }
  }
  .cell-5 {
    .mockups-wrapper {
      padding-top: 12px;
    }
  }
  img {
    width: 100%;
  }
  /* fix image styling on all project pages */
  //tempoary thing i did to style image
}
@media only screen and (min-width: 1024px) {
  section {
    padding: 64px;
  }
  .grid-container {
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    padding: 48px 0;
    .cell-5 {
      grid-column: 1/3;
      .mockups-wrapper {
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        gap: 24px;
        padding-top: 24px;
      }
    }
  }
  h2 {
    text-align: left;
    font-size: 32px;
    padding-bottom: 14px;
    &::after {
      transform: translateX(0);
      left: 0;
      width: 4%;
    }
  }
}
</style>
