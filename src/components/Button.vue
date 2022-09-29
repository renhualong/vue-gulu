<template>
  <button :class="{[`icon-${iconPosition}`] :true}">
    <svg v-if="icon" class="icon">
      <use :xlink:href="`#icon-${icon}`"></use>
    </svg>
    <div class="content">
      <slot>
      </slot>
    </div>
  </button>
</template>>
<script>
export default {
  props: ['icon', 'iconPosition']
}
</script>
<style lang="scss">
button {
  font-size: var(--font-size);
  height: var(--button-height);
  padding: 0 1em;
  border-radius: var(--button-radius);
  border: 1px solid var(--border-color);
  background: var(--button-bg);
  display: inline-flex;
  justify-content: center;
  align-items: center;
  vertical-align: middle;
  color: var(--button-color);
  cursor: pointer;

  >.icon {
    order: 1;
    margin-right: .3em;
  }

  >.content {
    order: 2;
  }

  &:hover {
    border-color: var(--button-color-hover);
  }

  &.icon-right {
    >.content {
      order: 1;
    }

    >.icon {
      order: 2;
      margin-right: 0;
      margin-left: .3em;
    }
  }

  &:active {
    background-color: var(--button-active-bg)
  }
}
</style>
