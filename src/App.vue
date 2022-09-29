



<template>
  <div>
    <Button icon="setting" icon-position="left">按钮</Button>
    <Button>按钮</Button>
    <Button icon="setting" icon-position="right">按钮</Button>
  </div>

</template>
<script>
import Button from './components/Button.vue'
export default {
  components: {
    Button
  }
}
</script>
<style>
.icon {
  width: 1em;
  height: 1em;
}
</style>
