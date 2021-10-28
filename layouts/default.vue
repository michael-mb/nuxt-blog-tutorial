<template>
  <div>
    <Header />
    <Nuxt />
  </div>
</template>

<script>
export default {
  name: "default"
}
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
}
body {
  background-color: #EEE;
}
a {
  text-decoration: none;
}
p {
  margin-bottom: 15px;
}
p:last-of-type {
  margin-bottom: 0px;
}
</style>
