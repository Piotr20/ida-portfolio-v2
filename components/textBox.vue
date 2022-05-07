<template>
  <section :id="scrollID">
    <h2>{{ text }}</h2>
  </section>
</template>

<script>
export default {
  name: 'TextBox',
  props: ['text', 'scrollID'],
}
</script>

<style lang="scss" scoped>
section {
  width: 100%;
  h2 {
    text-align: center;
    text-transform: uppercase;
    color: #f1ebe7;
    font-size: 52px;
    padding: 56px 0;
  }
}
@media only screen and (min-width: 1024px) {
  section {
    width: 100%;
    h2 {
      font-size: 96px;
      padding: 48px 0;
    }
  }
}
</style>
