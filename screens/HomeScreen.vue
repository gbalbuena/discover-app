<template>
  <view class="container">
    <text class="h1">Because you like</text>
    <text class="tag">vegan</text>
    <text class="tag">live-music</text>
    <text class="tag">salsa</text>
    <text class="tag">dancing</text>
    <text class="tag">wine</text>
    <text-input class="text-input-container" placeholder="tag" />
    <button title="Recommend me something" :on-press="onPressGoToList" />
    <button title="I'm feeling lucky" :on-press="onPressGoToDetails" />
  </view>
</template>

<style>
.h1 {
  font-size: 75;
}
.container {
}
.tag {
  width: 100;
  background-color: cornflowerblue;
  padding: 4;
  margin: 4;
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
  methods: {
    onPressGoToList: function() {
      this.navigation.navigate("List");
    },
    onPressGoToDetails: function() {
      this.navigation.navigate("Details");
    }
  }
}
</script>