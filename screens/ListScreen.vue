<template>
  <view class="container">
    <text class="h1">Recommendations</text>
    <view class="item">
      <text class="item-text"></text>
    </view>
    <view class="item">
      <button title="Ivy Precinct $$ >" :on-press="onPressGoToDetails" />
    </view>
    <view class="item">
      <button title="Establishment Bar $$$ >" :on-press="onPressGoToDetails2" />
    </view>

    <view class="item">
      <button title="Frankie's Pizza $$$ >" :on-press="onPressGoToDetails3" />
    </view>
  </view>
</template>

<style>
.h1 {
  font-size: 50;
}
.container {
}

.item {
  padding: 10;
}
.item-text {
  font-size: 30;
}
</style>

<script>
import React from 'react';
import { Text } from 'react-native';

export default {
  // Declare `navigation` as a prop
  props: {
    navigation: {
      type: Object
    }
  },
  methods: {
    onPressGoToDetails: function() {
      this.navigation.navigate("Details");
    },
    onPressGoToDetails2: function() {
      this.navigation.navigate("Details2");
    },
    onPressGoToDetails3: function() {
      this.navigation.navigate("Details3");
    }
  }
}
</script>