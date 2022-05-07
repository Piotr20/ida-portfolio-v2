<template>
  <section id="2-rows-grid">
    <h2 class="about-me-anim">Design og visuel identitet</h2>

    <!-- i need multiple headings, you made it weird -->

    <div class="grid-container">
      <div class="cell-1">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Asperiores,
          eius repellat voluptas obcaecati fuga distinctio voluptatum fugiat
          quasi maxime! Ea.
          <br /><br />
          We created a unique visual identity that carried through all. aspects
          of the business distingushes Smokepins ApS from other competitiors
          making their brand memorable. This project was not. as much for a
          coding as it was rather for design and marketing. Even though it was
          not very code-wise project we included. several immersive effects like
          e. g. lines drawing on scroll.
        </p>
      </div>
      <div class="cell-2">
        <img
          src="../../static/images/smokepins/smokepins-styletile.png"
          alt="Smokepins styletile"
        />
      </div>
      <div class="cell-3">
        <img
          src="../../static/images/smokepins/smokepins-closedbox.png"
          alt="Smokepins box closed"
        />
      </div>
      <div class="cell-4"></div>
      <div class="cell-5 heading-cell">
        <br /><br />

        <!-- i need multiple headings, you made it weird -->

        <h2 class="about-me-anim">Logo design</h2>
        <br />
      </div>
      <div class="cell-6"></div>
      <div class="cell-7">
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
}
.grid-container {
  padding: 24px 0;
  display: grid;
  grid-template-columns: 1fr;
  grid-template-rows: minmax(50%);
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
    padding-bottom: 14px;
    &::after {
      transform: translateX(0);
      left: 0;
      width: 4%;
    }
  }
}
</style>
