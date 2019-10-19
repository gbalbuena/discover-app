<template>
  <app-navigator></app-navigator>
</template>

<script>
import {
  createAppContainer,
  createStackNavigator,
} from "vue-native-router";

import LoginScreen from "./screens/LoginScreen.vue";
import WelcomeScreen from "./screens/WelcomeScreen.vue";
import HomeScreen from "./screens/HomeScreen.vue";
import DetailsScreen from "./screens/DetailsScreen.vue";
import DetailsScreen2 from "./screens/DetailsScreen2.vue";
import DetailsScreen3 from "./screens/DetailsScreen3.vue";
import ListScreen from "./screens/ListScreen.vue";

const StackNavigator = createStackNavigator(
  {
    Welcome: WelcomeScreen,
    Login: LoginScreen,
    Home: HomeScreen,
    Details: DetailsScreen,
    Details2: DetailsScreen2,
    Details3: DetailsScreen3,
    List: ListScreen
  },
  {
    initialRouteName: 'Login',
  }
);

const AppNavigator = createAppContainer(StackNavigator);

export default {
  components: { AppNavigator },
}
</script>