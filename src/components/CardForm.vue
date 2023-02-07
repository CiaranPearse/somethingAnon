<template>
  <div>
    <p class="text-lg font-bold">
      Card Details
    </p>
    <input
      v-model="cardNumber"
      type="text"
      class="block mb-3 text-pink-500 rounded"
      placeholder="Card Number"
      maxlength="16"
    >

    <input
      v-model="expiryDate"
      type="text"
      class="block mb-3 text-pink-500 rounded"
      placeholder="Expiry Date"
      maxlength="5"
    >

    <input
      v-model="cvc"
      type="text"
      class="block mb-3 text-pink-500 rounded"
      placeholder="CVC"
      maxlength="4"
    >

    <input
      v-model="cardHolder"
      type="text"
      class="block mb-3 text-pink-500 rounded"
      placeholder="Cardholder"
    >

    <select
      v-model="selectedCountry"
      class="block mb-3 text-sm rounded-lg"
    >
      <option
        disabled
        value=""
      >
        Please select one
      </option>
      <option>IE</option>
      <option>CHF</option>
    </select>

    <div class="block">
      <Price :country="selectedCountry" />
    </div>
  </div>
</template>

<script setup>
import Price from './Price.vue'
import { ref } from 'vue'
const cardNumber = ref('')
const expiryDate = ref('')
const cvc = ref('')
const cardHolder = ref('')
const selectedCountry = ref('IE')
</script>
