<template>
  <section id="2-rows-grid">

    <h2 class="about-me-anim">HEADING</h2>
    <div class="grid-container">
      <div class="cell-1">
        <p>some text here</p>
      </div>

      <div class="cell-2">
        <img src="" alt="" />
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
      //wHAT IS THIS ACTUALLY DOING
      display: flex;
      justify-content: center;
      align-items: center;
    } //the type is reffering to which grid box
  }
  p {
    padding-top: 10px;
    font-size: 16px;
    text-align: left;
    color: #95867d;
  }
}

@media only screen and (min-width: 1024px) {
  section {
    padding: 64px;
  }
  .grid-container {
    grid-template-columns: 1fr 1fr;
    grid-auto-rows: minmax(min-content, max-content);
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
}  
</style>
