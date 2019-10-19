<template>
  <view class="container">
    <scroll-view :content-container-style="{contentContainer: {
        paddingVertical: 20
    }}">
      <image
        :style="{width: 400, height: 400}"
        :source="{uri: 'https://media-cdn.tripadvisor.com/media/photo-s/0e/cc/0a/dc/restaurant-chocolat.jpg'}"
      />
      <text class="h1">{{ title }}</text>
      <text>{{ description }}</text>
      
      <image
      :style="{width: 50, height: 50}"
      :source="{uri: 'https://upload.wikimedia.org/wikipedia/commons/thumb/4/48/GoogleMaps_logo.svg/1024px-GoogleMaps_logo.svg.png'}"
      />
      <image
        :style="{width: 50, height: 50}"
        :source="{uri: 'https://upload.wikimedia.org/wikipedia/commons/thumb/e/e7/Instagram_logo_2016.svg/500px-Instagram_logo_2016.svg.png'}"
      />

      <text class="h2">Menu</text>
      <view class="item">
        <text class="item-text">Pizza $14</text>
      </view>
      <view class="item">
        <text class="item-text">Beer $7</text>
      </view>
      <view class="item">
        <text class="item-text">Pie $5</text>
      </view>

      <button title="Redeem money"></button>
      <button title="Order"></button>
      <button title="Currency conversion"></button>

      <text class="h2">Tip Etiquette</text>
      <text>Lorem ipsum dolor sit amet, consectetur adipiscing elit</text>

      <text class="h2">Tags</text>
      <text class="tag">vegan</text>
      <text class="tag">foodie</text>
      <text class="tag">live-music</text>
    </scroll-view>
  </view>
</template>

<style>
.h1 {
  font-size: 75;
  margin-bottom: 20;
}
.h2 {
  font-size: 45;
  margin-bottom: 10;
}

.container {
  margin: 10;
}
.item {
  padding: 10;
}
.item-text {
  font-size: 30;
}

.tag {
  width: 100;
  background-color: cornflowerblue;
  padding: 4;
  margin: 4;
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
      title: 'Establishment Bar',
      description: 'Stylish restaurants, a hip rooftop pool bar & big club nights in a landmark entertainment complex.'
    };
  },
  methods: {
    // goToHomeScreen() {
    //   this.navigation.navigate("Home");
    // }
  }
}
</script>