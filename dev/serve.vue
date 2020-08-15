<script>
import Vue from 'vue';
import { DonateUiKitSample } from '@/entry';

export default Vue.extend({
  name: 'ServeDev',
  components: {
    DonateUiKitSample,
  }
});
</script>

<template>
  <div id="app">
    <donate-ui-kit-sample />
  </div>
</template>
