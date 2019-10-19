<template>
  <view class="container">
    <text class="title">Where are you going?</text>
    <text-input
      class="text-input-container"
      placeholder="Type the location here"
      v-model="textContent"
    />
    <button title="Confirm" @press="goToHomeScreen"></button>
  </view>
</template>

<style scoped>
.title {
  font-size: 75;
}
.subtitle {
  font-size: 50;
}
.container {
  background-color: white;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-container {
  color: blue;
  padding: 2;
  font-size: 22;
}
.text-input-container {
  width: 300;
  height: 40;
  font-size: 22;
  border-color: gray;
}
</style>

<script>
export default {
  // Declare `navigation` as a prop
  props: {
    navigation: {
      type: Object
    }
  },

  data: function() {
    return {
      textContent: "",
      password: ""
    };
  },

  methods: {
    goToHomeScreen() {
      this.navigation.navigate("Home");
    }
  }
}
</script>