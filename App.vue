<template>
  <app-navigator></app-navigator>
</template>

<script>
import { createAppContainer, createStackNavigator } from "vue-native-router";
import SplashScreen from "./Splash";
import MainScreen from "./Main";

const StackNavigator = createStackNavigator(
  {
    Splash: SplashScreen,
    Main: MainScreen
  },
  {
    initialRouteName: "Splash",
    headerMode: "none"
  }
);

const AppNavigator = createAppContainer(StackNavigator);

export default {
  components: { AppNavigator }
};
</script>