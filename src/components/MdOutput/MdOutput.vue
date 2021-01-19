<template>
  <div class="mdoutput">
    <h1>OUTPUT<span>md output</span></h1>
    <article class="mdoutput__article" v-html="markedText"></article>
  </div>
</template>

<script>
import marked from "marked";
export default {
  name: "MdOutput",
  data() {
    return {};
  },
  props: {
    text: String,
  },
  computed: {
    markedText() {
      return marked(this.text);
    },
  },
};
</script>

<style scoped>
.mdoutput {
  flex: 1;
  display: flex;
  flex-direction: column;
  max-width: 50%;
  margin-left: 5px;
}
.mdoutput__article {
  flex: 1;
  outline: none;
  background: var(--body-color);
  border: none;
  border-radius: 5px;
  resize: none;
  padding: 10px;
  overflow-x: hidden;
  overflow-y: scroll;
}
.mdoutput > h1 {
  font-size: 20px;
  text-transform: uppercase;
  color: lightseagreen;
  cursor: pointer;
  font-weight: 500;
  user-select: none;
  user-zoom: none;
  display: flex;
  margin-bottom: 10px;
}
.mdoutput > h1 > span {
  background: lightseagreen;
  color: white;
  font-size: bold;
  font-size: 12px;
  text-transform: lowercase;
  padding: 2px 10px;
  border-radius: 999px;
  margin-left: 5px;
  height: fit-content;
}
</style>
