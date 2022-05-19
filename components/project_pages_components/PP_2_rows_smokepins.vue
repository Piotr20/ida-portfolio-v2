<template>
  <section id="2-rows-grid">

    <h2 class="about-me-anim">Brandets budskab</h2>
    <div class="grid-container">
      <div class="cell-1">
        <p>
          text here
          <!-- We created a unique visual identity that carried through all. aspects
          of the business distingushes Smokepins ApS from other competitiors
          making their brand memorable. This project was not. as much for a
          coding as it was rather for design and marketing. Even though it was
          not very code-wise project we included. several immersive effects like
          e. g. lines drawing on scroll. -->
        </p>
      </div>

      <div class="cell-2">
        <img src="../../static/images/smokepins/macbook-mockup-howto-trans.png" alt="macbook mockup webpage"/>
      </div>
      <div class="cell-3">
        <img src="../../static/images/smokepins/openbox.png" alt="smokepins box"/>
      </div>
      <div class="cell-4">
        <img src="../../static/images/smokepins/smokepins-closedbox.png" alt="smokepins box"/>
      </div>
    </div>

    <h2 class="about-me-anim">Design og visuel identitet</h2>
    <div class="grid-container">
      <div class="cell-5">
        <img src="../../static/images/smokepins/smokepins-styletile.png" alt="Styletile smokepins"/>
      </div>

      <div class="cell-6">
        <img src="../../static/images/smokepins/cards-mockups-smokepins.png" alt="mockups business card, logo"/>
      </div>
    </div>

    <div class="div-container">
      <div class="cell-7">
        <h3 class="about-me-anim">Logo design</h3>
        <p> 
          Det første logo var det Smokepins havde da vi begyndte at arbejde med dem.
          Herefter ses det logo som vi har udarbejdet. 
          Til sidst er logoet som firmaet endte ud med at designe selv, og som de benytter
          den dag idag.
          <!--           
            Faser: org, vores, nu 
          -->
        </p>
        <img class="hor" src="../../static/images/smokepins/logo-development-hor.png" alt=""/>
        <img class="ver" src="../../static/images/smokepins/logo-development-ver.png" alt=""/>
      </div>

<!--       <div class="cell-8">
        <img src="" alt=""/>
        <img src="" alt=""/>
      </div>
-->
    </div>


    <h2 class="about-me-anim">Content</h2>
    <div class="grid-container">
      <div class="cell-9">
        <img src="" alt=""/>
      </div>

      <div class="cell-10">
        <img src="" alt=""/>
      </div>
    </div>

    <div class="grid-container">
      <div class="cell-11">
        <h3>Infographic</h3>
        <p>
          infographic text
        </p>
      </div>

      <div class="cell-12">
        <img src="../../static/images/smokepins/infographic.png" alt="infographic"/>
      </div>
    </div>

    <h2 class="about-me-anim">Some Content</h2>
    <div class="grid-container">
      <div class="cell-13">
        <h3>Infographic</h3>
        <p>
          infographic text
        </p>
      </div>

      <div class="cell-14">
        <img src="../../static/images/smokepins/infographic.png" alt="infographic"/>
      </div>
    </div>

  <h2 class="about-me-anim">Website</h2>
    <div class="div-container">
      <div class="cell-15">
        <video
          id="video-2"
          src="../../static/images/smokepins/screencast-mockup.mp4"
          controls
          autoplay
          loop
          muted
        ></video>
      </div>
    </div>
  <!-- 
    <h2 class="about-me-anim">heading</h2>
    <div class="grid-container">
      <div class="cell-15">
      </div>
    </div>
  -->

  </section>
</template>

<script>
export default {
  name: 'TwoRowsLayout_smokepins',
  props: {
    headingText: String,
  },
}
</script>

<style lang="scss" scoped>
section {
  background-color: #f1ebe7;
  padding: 32px;
  p {
    padding-top: 10px;
    font-size: 16px;
    text-align: left;
    color: #95867d;
  }
}

h2 {
  color: #95867d;
  text-transform: uppercase;
  font-size: 32px;
  padding-bottom: 15px;
  position: relative;
  text-align: center;
  &::after {
    content: '';
    position: absolute;
    width: 50%;
    height: 4px;
    background-color: #95867d;
    left: 50%;
    bottom: 0;
    transform: translate(-50%, -50%);
    }
  }
  h3 {
  color: #95867d;
  font-weight: bold;
  text-transform: uppercase;
  font-size: 20px;
  padding-bottom: 20px;
  position: relative;
  text-align: center;
}
.grid-container {
  padding: 20px 0 80px;
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
      //wHAT IS THIS ACTUALLY DOING
      display: flex;
      justify-content: center;
      align-items: center;
    } //the type is reffering to which grid box
  }
}
.div-container{
  padding: 20px 0 80px;
  div {
    text-align: left;
    &:nth-of-type(2) {
      display: flex;
      justify-content: center;
      align-items: center;
      }
    }
  .hor{
    display: none !important; //this suddenly didnt work?
  }
  .ver{
    display: block;
    width: 80%;
    padding-top: 30px;
    margin: auto;
  }
  }
  .cell-15{
    video{
      width: 100%;
      margin: auto;
    }
  }

@media only screen and (min-width: 1024px) {
  section {
    padding: 64px;
  }
  .grid-container {
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr;
  }
  // .grid-container-2-rows {
  //   grid-template-columns: 1fr 1fr;
  //   grid-template-rows: 1fr;
  // }
  h2 {
    text-align: left;
    font-size: 32px;
    padding-bottom: 40px;
    height: 80px; 
    &::after {
      transform: translate(0);
      left: 0;
      width: 8%;
    }
  }
  h3 {
    text-align: left;
    font-size: 20px;
    padding-bottom: 10px;
    height: 40px;
    font-weight: bold;
    }
  p {
    padding-top: 0px !important;
    font-size: 16px;
    text-align: left;
    color: #95867d;
  }
  .div-container{
    .hor{
      display: block !important;
      padding-top: 30px;
    }
    .ver{
      display: none;
    }
    p {
      max-width: 50%;
    }
  }
  .cell-7{
    img{
      width: 100%;
    }
  }
  .cell-15{
    video{
      width: 70%;
      margin: auto;
    }
  }
}
</style>
