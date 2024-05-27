<template>
  <div class="parent-container">
    <h2>Parent Component</h2>
    <div class="child-wrapper">
      <slot></slot>
      <ChildComponent @childEvent="handleChildEvent" />
    </div>
    <p>Data from child: {{ childData }}</p>
  </div>
</template>

<script>
import ChildComponent from './ChildComponent.vue';

export default {
  components: {
    ChildComponent,
  },
  data() {
    return {
      childData: '',
    };
  },
  methods: {
    handleChildEvent(data) {
      this.childData = data;
    },
  },
};
</script>


<style>
.parent-container {
  border: 1px solid #ccc;
  padding: 20px;
  margin-bottom: 20px;
}

.child-wrapper {
  margin-bottom: 15px;
}


</style>