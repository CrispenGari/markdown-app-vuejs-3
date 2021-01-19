<template>
  <div class="header">
    <h1>Home</h1>
    <h1>Markdown App</h1>
  </div>
</template>

<script>
export default {
  name: "Header",
};
</script>
<style scoped>
.header {
  background: var(--header-color);
  color: white;
  z-index: 1;
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
  position: sticky;
  top: 0;
  padding: 20px;
  user-select: none;
  user-zoom: none;
}
.header > h1 {
  font-size: 16px;
  text-transform: uppercase;
  letter-spacing: 2px;
  cursor: pointer;
  font-weight: 500;
}
</style>
