<template>
  <section id="2-rows-grid">

    <h2 class="about-me-anim">Brandets budskab</h2>
    <div class="grid-container">
      <div class="cell-1">
      </div>

      <div class="cell-2">
        <img src="../../static/images/country_wellness/country-wellness-business-card-mockup.png" alt="" />
      </div>

      <div class="cell-3"></div>

      <div class="cell-4">
        <img src="" alt="" />
      </div>

      <div class="cell-5"></div>
    </div>

    <h2 class="about-me-anim">Design og visuel identitet</h2>
    <div class="grid-container">
      <div class="cell-3">
        <img src="" alt="" />
      </div>

      <div class="cell-4">
        <img src="" alt="" />
      </div>
    </div>

    <h2 class="about-me-anim">Logo design</h2>
    <div class="grid-container">
      <div class="cell-5">
        <p>some text here</p>
      </div>

      <div class="cell-6">
        <img src="" alt="" />
      </div>
    </div>
    
    <h2 class="about-me-anim">Content</h2>
    <div class="grid-container">
      <div class="cell-7">
        <img src="" alt=""/>
      </div>

      <div class="cell-8">
        <img src="" alt=""/>
      </div> 
    </div>

    <h2 class="about-me-anim">Website</h2>
    <div class="grid-container">
      <div class="cell-9">
        <img src="" alt=""/>
      </div>

      <div class="cell-10">
        <img src="" alt=""/>
      </div> 
    </div>

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
  grid-auto-rows: minmax(min-content, max-content);
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
  }
}
@media only screen and (min-width: 1024px) {
  section {
    padding: 64px;
  }
  .grid-container {
    padding: 48px 0;
  }
  h2 {
    text-align: left;
    font-size: 32px;
    padding-bottom: 20px;
    &::after {
      transform: translateX(0);
      left: 0;
      width: 4%;
    }
  }
}
</style>
