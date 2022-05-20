<template>
  <section id="language">
    <h2 class="language-anim">SPROG</h2>
    <p class="language-anim">
      Gennem min internationale uddannelse, som Multimediedesigner på
      Erhvervsakademiet Aarhus, har jeg udviklede mine sproglige egenskaber,
      samt udvidet min kulturelle forståelse.
      <br />
      <br />
      Erhvervsakademiet Aarhus har interviewet mig til en artikel netop omkring
      det at studere på engelsk.
    </p>
    <a
      class="language-anim"
      href="https://www.eaaa.dk/videregaende-uddannelser/erhvervsakademiuddannelse/multimedia-design/ida-har-bragt-verden-hjem-til-sig/"
      target="_blank"
      >Læs artikel</a
    >
    <div class="flags-container">
      <div class="language-anim">
        <img src="../static/images/flag-dk.png" alt="Danish flag" />
        <div>
          <span>DANSK</span><br /><span>
            <ul>
              <li>Forståelse: Modersmål</li>
              <li>Tale: Modersmål</li>
              <li>Læse: Modersmål</li>
              <li>Skrive: Modersmål</li>
            </ul>
          </span>
        </div>
      </div>
      <div class="language-anim">
        <img src="../static/images/flag-uk.png" alt="British flag" />

        <div>
          <span>ENGELSK</span> <br /><span>
            <ul>
              <li>Forståelse: Flydende</li>
              <li>Tale: Flydende</li>
              <li>Læse: Flydende</li>
              <li>Skrive: Flydende</li>
            </ul>
          </span>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'Language',
  mounted: function () {
    this.$gsap.from('.language-anim', {
      scrollTrigger: {
        trigger: '#language',
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
  background-color: #e54575;
  padding: 32px;
  margin: 24px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  h2 {
    text-transform: uppercase;
    color: white;
    font-size: 32px;
    padding-bottom: 32px;
    margin-bottom: 24px;
    position: relative;
    text-transform: uppercase;
    &::after {
      content: '';
      position: absolute;
      width: 50%;
      height: 5px;
      background-color: #fff;
      left: 50%;
      bottom: 0;
      transform: translate(-50%, -50%);
    }
  }
  p {
    color: white;
    font-size: 18px;
    width: 100%;
    text-align: center; //Check if this works!!
  }
}
.flags-container {
  padding-top: 64px;
  display: flex;
  flex-direction: column;
  & > div {
    width: fit-content;
    display: flex;
    align-items: center;
    margin-bottom: 16px;
    img {
      width: 50px;
    }
  }
  div {
    color: white;
    font-size: 18px;
    text-align: left;
    padding-left: 32px;
    span {
      font-weight: 600;
    }
    span:nth-of-type(2) {
      font-weight: 300;
      font-size: 14px;
    }
  }
}
a {
  text-transform: uppercase;
  background-color: #fff;
  color: #e54575;
  font-size: 18px;
  padding: 8px 30px;
  display: inline-block;
  margin-top: 24px;
  transition: all 0.3s ease;
  border: 3px solid #fff;
  cursor: pointer;
  text-decoration: none;
  font-weight: 600;
  &:hover {
    background-color: #e54575;
    color: #fff;
  }
}

@media only screen and (min-width: 1024px) {
  section {
    width: 100%;
    padding: 64px;
    margin: 36px 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    h2 {
      font-size: 32px;
      padding-bottom: 20px;
    }
    p {
      font-size: 18px;
      width: 75ch;
    }
    a {
      padding: 6px 16px;
      font-size: 18px;
      text-transform: uppercase;
      background-color: #fff;
      color: #e54575;
      padding: 10px 35px;
      display: inline-block;
      margin-top: 24px;
      transition: all 0.3s ease;
      border: 3px solid #fff;
      cursor: pointer;
      text-decoration: none;
      font-weight: 600;
      &:hover {
        background-color: #e54575;
        color: #fff;
      }
        }
      }
  .flags-container {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding-top: 50px;
    div {
      margin: 12px 0;
      font-size: 20px;
      align-items: center;
      display: flex;
      justify-content: center;
      img {
        width: 70px;
      }
      br {
        display: none;
      }
      div {
        display: flex;
        flex-direction: column;
        align-items: flex-start;
        span:nth-of-type(2) {
          margin-top: 6px;
          font-size: 16px;
        }
      }
    }
    h3 {
      font-size: 20px;
    }
  }
}
</style>
