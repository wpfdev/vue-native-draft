<template>
  <view class="container">
    <text class="text-color-primary h1">{{header}}</text>
    <text class="text-color-primary">{{message}}</text>
    <text class="text-color-primary down-fixed">...Loading...</text>
  </view>
</template>

<script>
export default {
  data() {
    return {
      header: "aprogrammer.ru",
      message: "The Full-Stack Freelancer"
    };
  },
  mounted() {
    setTimeout(() => {
      this.navigation.navigate("Main");
    }, 3000);
  },
  props: {
    navigation: {
      type: Object
    }
  }
};
</script>

<style>
.container {
  background-color: #fff;
  align-items: center;
  justify-content: center;
  flex: 1;
}
.text-color-primary {
  color: blue;
}
.h1 {
  font-size: 30;
}
.down-fixed {
  position: absolute;
  bottom: 50;
}
</style>
