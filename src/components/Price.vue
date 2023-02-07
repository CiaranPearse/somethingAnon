<template>
  <div>
    <p v-if="country === 'IE'">
      € 25<sup>95</sup> / Annual
    </p>
    <p v-if="country === 'CHF'">
      CHF 50 / Annual
    </p>
    <p v-else />
  </div>
</template>

<script setup>
// eslint-disable-next-line vue/require-prop-types
const props = defineProps(['country'])

console.log(props.country)
</script>