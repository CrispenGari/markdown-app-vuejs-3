<template>
  <div class="mdfile">
    <h1>README.MD <span>md file</span></h1>
    <textarea class="mdfile__text" v-model="text" @keyup="sendText"></textarea>
  </div>
</template>

<script>
export default {
  name: "MdFile",
  data() {
    return {
      text: "",
    };
  },
  methods: {
    sendText() {
      this.$emit("text", this.text);
    },
  },
};
</script>

<style scoped>
.mdfile {
  flex: 1;
  display: flex;
  flex-direction: column;
  max-width: 50%;
  margin-right: 5px;
}
.mdfile__text {
  flex: 1;
  outline: none;
  background: var(--body-color);
  border: none;
  border-radius: 5px;
  resize: none;
  padding: 10px;
}
.mdfile__text:--webkit-scrollbar {
  display: none;
}
.mdfile > h1 {
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
.mdfile > h1 > span {
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
