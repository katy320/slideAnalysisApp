<template>
  <div id="app">
  <AppHeader/>
  <AppBody/>
  </div>
</template>

<script>
import AppHeader from "@/components/AppHeader"
import AppBody from "@/components/AppBody"

export default {
  components: {
    AppHeader,
    AppBody
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto');
:root {
  --blue: #011F5B;
  --red: #990000;
  --gray: #44464B;
  --dark-gray: #131315;
  --light-gray: #f2f2f3;
  --green: #008200;
  --panelWidth: 700px;
}
* { 
  font-family: "Roboto", "Open Sans", sans-serif;
}
#app {
  text-align: center;
}
body {
  margin: 0;
}
</style>
