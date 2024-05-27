<template>
  <div>
    <h4>Grandchild Component</h4>
    <button @click="emitData">Emit Data</button>
  </div>
</template>

<script>
export default {
  methods: {
    emitData() {
      this.$emit('grandchildEvent', 'Data from grandchild');
    },
  },
};
</script>
