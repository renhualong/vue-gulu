<template>
  <button>按钮</button>
</template>>
<script>
export default {

}
</script>
<style>
button {
  font-size: var(--font-size);
  height: var(--button-height);
  padding: 0 1em;
  border-radius: var(--border-radius);
  border: 1px solid var(--border-color);
  background: var(--button-bg);
  color: var(--button-color);
  cursor: pointer;
}

button:hover {
  border-color: var(--button-color-hover);
}

button:active {
  background-color: var(--button-active-bg)
}
</style>