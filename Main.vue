<template>
  <web-view :source="{uri: 'http://aprogrammer.ru'}" :style="{marginTop: 0}" />
</template>
<script>
import { WebView } from "react-native-webview";

export default {
  name: "myComponent",
  components: {
    "web-view": WebView
  }
};
</script>