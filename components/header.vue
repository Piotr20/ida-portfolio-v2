<template>
  <header>
    <NuxtLink to="/">
      <img src="../static/images/logo.png" alt="Ida Skjødt Olesen logo" />
    </NuxtLink>
    <nav>
      <NuxtLink to="/">Hjem</NuxtLink>
      <a href="#portfolio">Portfolio</a>
      <a href="#about">Om mig</a>
      <a href="#cv">CV</a>
      <a href="#contact">Kontakt mig</a>
    </nav>
    <div @click="displayBurger = !displayBurger" class="burger">
      <font-awesome-icon class="burger-icon" icon="fa-solid fa-bars" />
    </div>
    <div class="burger-curtain" :class="{ active: displayBurger }">
      <div class="gradient-overlay">
        <div
          class="burger-close-container"
          @click="displayBurger = !displayBurger"
        >
          <font-awesome-icon class="burger-close" icon="fa-solid fa-xmark" />
        </div>

        <ul class="burger-nav">
          <li><a @click="displayBurger = false" href="#home">Home</a></li>
          <li>
            <a @click="displayBurger = false" href="#portfolio">Portfolio</a>
          </li>
          <li><a @click="displayBurger = false" href="#about">About</a></li>
          <li><a @click="displayBurger = false" href="#contact">Contact</a></li>
        </ul>
        <a class="logo-curtain" @click="displayBurger = false" href="#">
          <img
            src="../static/images/logo_white.png"
            alt="Ida Skjødt Olesen
          logo"
        /></a>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      displayBurger: false,
    }
  },
  name: 'Header',
}
</script>

<style scoped lang="scss">
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  width: 100%;
  height: 8vh;
  background-color: #f1ebe7;
  padding: 0 32px;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 100;
  box-shadow: 1px 1px 8px 3px rgba(0, 0, 0, 0.25);
}
header > a {
  height: 100%;
}
header img {
  height: 100%;
}
nav {
  display: none;
}
.burger-curtain {
  position: fixed;
  width: 100%;
  height: 100vh;
  right: -100%;
  top: 0;
  transition: right 0.4s ease-in-out;
}
.gradient-overlay {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  background: linear-gradient(
    135deg,
    #ff5b459d 0%,
    #ff68b696 45%,
    #b555e296 100%
  );
  backdrop-filter: blur(14px) opacity(100%);
}
.burger-curtain.active {
  right: 0;
}
.burger-icon {
  font-size: 26px;
}
.burger-close-container {
  align-self: flex-end;
  height: 8vh;
  line-height: 8vh;
  padding-right: 32px;
}
.burger-close-container .burger-close {
  font-size: 36px;
  margin-top: 16px;
  color: white;
}
.burger-nav {
  list-style: none;
  margin-top: 42vh;
  transform: translateY(-50%);
  li {
    padding: 18px 0;
    border-bottom: 2px solid white;
    &:nth-last-of-type(1) {
      border-bottom: none;
    }
    a {
      text-decoration: none;
      font-size: 28px;
      color: white;
    }
  }
}
.logo-curtain {
  height: 12.5%;
  display: flex;
  margin-top: 12px;
  align-self: center;
  align-items: center;
  justify-content: center;
  img {
    width: 100%;
    object-fit: contain;
    object-position: center;
  }
}
@media only screen and (min-width: 1024px) {
  header {
    height: 9vh;
    justify-content: left;

    & > a {
      height: 90%;
      justify-self: start;
    }
  }
  nav {
    display: flex;
    position: absolute;
    left: 50%;
    transform: translateX(-50%);
    a {
      text-transform: uppercase;
      font-size: 18px;
      text-decoration: none;
      color: #95867d;
      padding: 6px 16px;
      margin: 0 30px;
      position: relative;
      white-space: nowrap;

      &::after {
        position: absolute;
        left: 0;
        bottom: 0;
        content: '';
        width: 0;
        height: 1.5px;
        background-color: #95867d;
        transition: all 0.3s ease-in;
      }
      &:hover::after {
        width: 100%;
      }
    }
  }
  .burger {
    display: none;
  }
  .burger-curtain {
    display: none;
  }
}
</style>
