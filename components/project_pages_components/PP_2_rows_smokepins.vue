<template>
  <section id="2-rows-grid">
    <h2 class="about-me-anim">Design og visuel identitet</h2>

    <div class="grid-container">
      <div class="cell-1">
        <p>
          Smokepins har en meget personlig kommunikation med deres målgruppe, hvilket nok bunder
          i at Ole (virksomhedsejer) selv er en del af målgruppen. Ole vil gerne dele et produkt
          med folk lige som ham, folk der holder af friluftslivet. Det handler ikke om marketing der
          er 'in your face', det handler om at skabe en forbindelse til et 'comunity'.
          <br><br>
          Fordi Smokepins er unikt og har et niche marked (endnu), er det vigtigt at skabe en solid 
          relation til kunderne, med fokus på tilbagevendende kunder. 
          <br><br>
          Det er essientielt at udvide markedet til kunder som måske ikke vidste at Smokepins&reg; 
          netop lige er det de står og mangler. Folk som elsker at udforske deres smagsløg, 
          folk som holder af at bruge tid på at forberede deres mad, på en måde der forener 
          dem med deres forfædre.
        </p>
      </div>
      <div class="cell-2">
        <img
          src=""
          alt="Smokepins styletile"
        />
      </div>
      <div class="cell-3">
        <img
          src=""
          alt="Smokepins box closed"
        />
      </div>
      <div class="cell-4"></div>
      <div class="cell-5 heading-cell">
        <br /><br />

        <!-- i need multiple headings, you made it weird -->

        <h2 class="about-me-anim">Logo design</h2>
        <br />
        <img src=""
          alt="Smokepins logo"/>
      </div>
      <div class="cell-6"></div>
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
        <img src="../../static/images/smokepins/instructions-brochure-crop.png" alt="instructions brochure"/>
      </div>

      <div class="cell-10">
        <img src="../../static/images/smokepins/iphone-some-bg.png" alt="instructions brochure"/>
      </div> 
    </div>

    <div class="grid-container">
      <div class="cell-11">
        <h3>Infographic</h3>
        <p>
          Lorem, ipsum dolor sit amet consectetur adipisicing elit. Reiciendis
          recusandae distinctio vel eos, nemo eum perferendis temporibus minima
          quam odit, rerum obcaecati est similique qui? Eveniet magni eum odit
          sapiente.
        </p>
      </div>
      <div class="cell-8">
        <img
          src="../../static/images/smokepins/smokepins-logo-all.png"
          alt="Smokepins logo"
        />
      </div>
    </div>
<!-- 
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
 -->
  <h2 class="about-me-anim">Website</h2>
    <div class="div-container">
      <div class="cell-15">
        <video
          id="video"
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
}
h2 {
  color: #95867d;
  text-transform: uppercase;
  font-size: 32px;
  padding-bottom: 20px;
  position: relative;
  p {
    font-size: 20px;
    font-family: 'Lato', sans-serif;
    text-align: left;
    color: #95867d;
  }
  /* dunno what i did here */
  //why is this not working?!

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
  h3 {
  color: #95867d;
  font-weight: bold;
  text-transform: uppercase;
  font-size: 20px;
  padding-bottom: 10px;
  position: relative;
  text-align: center;
}
.grid-container {
  padding: 20px 0 60px;
  display: grid;
  grid-template-columns: 1fr;
  grid-auto-rows: minmax(min-content, max-content);
  grid-gap: 24px;
  & > div {
    display: flex;
    justify-content: center;
    align-items: center;
    &.heading-cell {
      justify-content: center;
    } //the type is reffering to which grid box
    &:nth-of-type(1) {
      align-items: flex-start;
    }
  }

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
  .cell-2{
    img{
      width: 100%;
    }
  }
  .cell-15{
    video{
      width: 100%;
      margin: auto;
    }
  }
}
img {
  width: 100%;
}
/* fix image styling on all project pages */
//tempoary thing i did to style image

@media only screen and (min-width: 1024px) {
  section {
    padding: 64px;
  }
  .grid-container {
    padding: 48px 0;
    grid-template-columns: 1fr 1fr;
    & > div {
      &.heading-cell {
        justify-content: flex-start;
      } //the type is reffering to which grid box
    }
  }
  h2 {
    text-align: left;
    font-size: 32px;
    padding-bottom: 20px;
    &::after {
      transform: translateX(0);
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
      max-width: 48%;
    }
  }
  .cell-2{
    img{
      width: 70%;
    }
  }
  .cell-7{
    img{
      width: 100%;
    }
  }
  .cell-15{
    video{
      width: 60%;
      margin: auto;
    }
  }
}
</style>
