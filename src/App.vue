<template>
  <div class="app">
    <Header />
    <div class="app__main">
      <MdFile @text="reciveText" />
      <MdOutput :text="text" />
    </div>
  </div>
</template>

<script>
import { Header, MdFile, MdOutput } from "./components";
export default {
  name: "App",
  components: {
    Header,
    MdOutput,
    MdFile,
  },
  data() {
    return {
      text: "",
    };
  },
  methods: {
    reciveText(prop) {
      this.text = prop;
    },
  },
};
</script>

<style scoped>
.app {
  display: flex;
  flex-direction: column;
  width: 100vw;
  height: 100vh;
}
.app__main {
  display: flex;
  flex-wrap: wrap;
  width: 100%;
  max-width: 1000px;
  padding: 10px;
  border: 1px solid lightgray;
  border-radius: 5px;
  margin: 10px auto;
  flex: 1;
  background: white;
}
</style>
