<script setup lang="ts">
const cookie24Days = useCookie('cookie24Days', { default: () => false, maxAge: 24 * 24 * 60 * 60 })
const cookie25Days = useCookie('cookie25Days', { default: () => false, maxAge: 25 * 24 * 60 * 60 })
const cookie30Days = useCookie('cookie30Days', { default: () => false, maxAge: 30 * 24 * 60 * 60 })
const cookie365ChromeDays = useCookie('cookie365ChromeDays', { default: () => false, maxAge: 1704085200 })
const cookie400ChromeDays = useCookie('cookie400ChromeDays', { default: () => false, maxAge: 1707109200 })
const cookie365Days = useCookie('cookie365Days', { default: () => false, maxAge: 365 *  24 * 60 * 60 })
const cookie365DaysObject = useCookie('cookie365DaysObject', { default: () => ({ val: false }), maxAge: 365 *  24 * 60 * 60 })
</script>

<template>
  <div>
    <span class="success">&#x2713;</span>
    <button @click="cookie24Days = !cookie24Days">24 days</button>
    {{ cookie24Days }}
  </div>

  <div>
    <span class="error">&#x10102;</span>
    <button @click="cookie25Days = !cookie25Days">25 days</button>
    {{ cookie25Days }}
  </div>

  <div>
    <span class="error">&#x10102;</span>
    <button @click="cookie30Days = !cookie30Days">30 days</button>
    {{ cookie30Days }}
  </div>

  <div>
    <span class="error">&#x10102;</span>
    <button @click="cookie365ChromeDays = !cookie365ChromeDays">365 days (Chrome LOL)</button>
    {{ cookie365ChromeDays }}
  </div>

  <div>
    <span class="success">&#x2713;</span>
    <button @click="cookie400ChromeDays = !cookie400ChromeDays">400 days (Chrome LOL)</button>
    {{ cookie400ChromeDays }}
  </div>

  <div>
    <span class="success">&#x2713;</span>
    <button @click="cookie365Days = !cookie365Days">365 days</button>
    {{ cookie365Days }}
  </div>

  <div>
    <span class="error">&#x10102;</span>
    <button @click="cookie365DaysObject.val = !cookie365DaysObject.val">365 days (object)</button>
    {{ cookie365DaysObject.val }}
  </div>

  <div>PS: Last two cookie refs seem to interact with each other, try pressing the 2 buttons alternatively</div>
</template>

<style scoped>
.error { color: red; }
.success { color: green; }
.error, .success { margin-inline-end: 8px; display: inline-block; width: 16px; text-align: center; }
div { margin-bottom: 12px; }
button { margin-inline-end: 8px; }
</style>
