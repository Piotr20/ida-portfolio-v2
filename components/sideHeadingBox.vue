<template>
  <div class="heading-box">
    <h2 class="">{{ title }}</h2>
  </div>
</template>

<script>
export default {
  name: 'SideHeading',
  props: ['title'],
}
</script>

<style lang="scss" scoped>
.heading-box {
  width: 100%;
  height: 100%;
  background-color: #f1ebe7;
  padding: 32px;
  h2 {
    color: #95867d;
    text-transform: uppercase;
    font-size: 32px;
    padding-bottom: 14px;
    position: relative;
    text-align: center;

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
}
@media only screen and (min-width: 1024px) {
  .heading-box {
    padding: 64px;
    h2 {
      text-align: left;
      font-size: 32px;
      &::after {
        transform: translateX(0);
        left: 0;
        width: 20%;
      }
    }
  }
}
</style>
