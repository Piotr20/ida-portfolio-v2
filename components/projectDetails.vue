<template>
  <section>
    <div class="client-details">
      <h2>Kunde</h2>
      <h3>{{ client }}</h3>
    </div>
    <div class="services-details">
      <h2>SERVICES</h2>
      <ul>
        <template v-for="(service, index) in services">
          <li :key="index">
            <h3>{{ service }}</h3>
          </li>
        </template>
      </ul>
    </div>
    <div class="tools-details">
      <h2>Værktøjer</h2>
      <div class="grid-container">
        <template v-for="(image, index) in toolsSrc">
          <img :src="image.src" alt="tool icon" :key="index" />
        </template>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ProjectDetails',
  props: {
    client: String,
    services: Array,
    toolsSrc: Array,
    purposeText: String,
  },
  mounted: function () {
    console.log(this.toolsSrc)
  },
}
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  margin: 24px 0;
  display: grid;
  gap: 24px;
  div {
    padding: 32px;
    h2 {
      text-transform: uppercase;
      color: white;
      font-size: 32px;
      padding-bottom: 32px;
      margin-bottom: 32px;
      position: relative;
      text-transform: uppercase;
      text-align: left;
      &::after {
        content: '';
        position: absolute;
        width: 40%;
        height: 5px;
        background-color: #fff;
        left: 0;
        bottom: 0;
        transform: translate(0);
      }
    }
    p {
      color: #95867d;
      font-size: 18px;
    }
    h3 {
      color: white;
      font-size: 22px;
      text-align: left;
    }
    ul {
      list-style: none;
      li {
        padding: 2px 0;
      }
    }
  }
}
.client-details {
  background-color: #a093f0;
}
.services-details {
  background-color: #e54575;
}
.tools-details {
  background-color: #e877c1;
}
.grid-container {
  display: grid;
  width: 100%;
  padding: 0;
  grid-template-columns: repeat(4, 1fr);
  gap: 24px;
  align-items: center;
  justify-items: center;
  img {
    width: 100%;
  }
}
.purpose {
  background-color: #f1ebe7;
  h2 {
    color: #95867d;
    text-align: center;

    &::after {
      background-color: #95867d;
      transform: translateX(-50%);
      left: 50%;
    }
  }
}
@media only screen and (min-width: 1024px) {
  section {
    margin: 36px 0;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 36px;
    div {
      padding: 64px;
      h2 {
        font-size: 32px;
        padding-bottom: 14px;
        margin-bottom: 24px;

        text-align: left;
        &::after {
          width: 20%;
          left: 0;
          transform: translateX(0);
        }
      }
      p {
        font-size: 20px;
        text-align: left;
      }
      h3 {
        font-size: 22px;
      }
    }
  }
  .grid-container {
    gap: 36px;
    align-items: center;
    justify-items: center;
    grid-template-columns: repeat(5, 1fr);
    img {
      width: 100%;
    }
  }
  .purpose {
    grid-column: 1/4;
    h2 {
      &::after {
        width: 10%;
      }
    }
    p {
      text-align: center;
      width: 80ch;
      margin: 0 auto;
    }
  }
}
</style>
