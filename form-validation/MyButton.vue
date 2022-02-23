<template>
  <button v-bind:style="{ background, color }" v-bind:disabled="disabled">
    Button
  </button>
</template>

<script>
export default {
  props: {
    background: {
      type: String,
    },
    color: {
      type: String,
    },
    disabled: {
      type: Boolean,
    },
  },
};
</script>

/* Scoped will make sure that all of the styles will be applied for this
template ONLY! */
<style scoped>
button:disabled {
  opacity: 0.5;
}

button {
  background: none;
  color: black;
  border: none;
  border-radius: 5px;
  padding: 10px 40px;
  font-size: 16px;
  cursor: pointer;
}

button:hover {
  filter: brightness(125%);
}
</style>
