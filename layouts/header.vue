<template>
  <div>
    <header>
      <slot name="header"> Default header content </slot>
    </header>
  </div>
</template>

<script>
export default {
  layout: 'header',
}
</script>
