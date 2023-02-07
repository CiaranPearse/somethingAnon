<template>
  <div>
    <preview-card
      cc-number="4111111111111111"
      expiration="04/25"
      ccv="333"
    />
    <card-form />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

import PreviewCard from '../components/PreviewCard.vue'
import CardForm from '../components/CardForm.vue'

export default defineComponent({
  components: {
    PreviewCard,
    CardForm,
  },
})
</script>
