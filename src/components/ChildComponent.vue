<template>
  <div class="child-container">
    <h3>Child Component</h3>
    <GrandchildComponent @grandchildEvent="handleGrandchildEvent" />
  </div>
</template>

<script>
import GrandchildComponent from './GrandchildComponent.vue';

export default {
  components: {
    GrandchildComponent,
  },
  methods: {
    handleGrandchildEvent(data) {
      this.$emit('childEvent', data);
    },
  },
};
</script>


<style>
.child-container {
  border: 1px solid #999;
  padding: 15px;
  margin-bottom: 15px;
}

</style>