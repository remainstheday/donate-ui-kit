<template>
  <div class="donate-card">
    <header v-if="!hidePoster" class="card-header">
      <img :src="posterImage" />
    </header>
    <main class="card-body">
      <div class="title">
        <img v-if="logoImage" :src="logoImage" class="logo" />
        <strong v-if="title">{{ title }}</strong>
        <p v-if="subtitle">{{ subtitle }}</p>
      </div>
      <div class="progress-container">
        <div class="progress-details">
          <strong>{{ amountRaised }}</strong>
          <strong>{{ amountGoal }}</strong>
        </div>
        <div class="progress-bar"></div>
      </div>
      <p class="description">{{ description }}</p>
    </main>
    <footer>
      <button @click="onDonateBtnClick">{{ buttonText }}</button>
    </footer>
  </div>
</template>

<script>
import placeholder from "./placeholder.svg";

export default {
  name: "donate-card",
  props: {
    posterImage: {
      type: String,
      default: placeholder
    },
    logoImage: {
      type: String,
      default: placeholder
    },
    hidePoster: {
      type: Boolean,
      default: false
    },
    title: {
      type: String,
      default: "card Title"
    },
    subtitle: {
      type: String,
      default: "card Title"
    },
    buttonText: {
      type: String,
      default: "Donate"
    }
  },
  methods: {
    onDonateBtnClick() {
      this.$emit("donateBtnClick");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.donate-card {
  border: 1px solid rgba(0, 0, 0, 0.125);
  width: 250px;
  height: 300px;
  margin: 5px;
}

button {
  width: 95%;
  background: #3541e0;
  border: 0;
  border-radius: 3px;
  color: #fff;
  cursor: pointer;
  padding: 10px;
  margin: 5px auto;
}
</style>
