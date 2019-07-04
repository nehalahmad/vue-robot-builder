<template>
  <div>
    <div class="header">
      <span v-if="open" @click="open = !open">&#x25B2; Collapse</span>
      <span v-if="!open" @click="open = !open">&#x25BC; Expand</span>
    </div>

    <!-- Toggleable content here -->
    <slot v-if="open">
      <div>Default content goes here</div>
    </slot>
  </div>
</template>

<script>
export default {
  name: "CollapsibleSection",
  data: () => ({ open: true })
};
</script>

<style scoped>
.header {
  background-color: #bbb;
  padding: 3px;
  cursor: pointer;
  text-align: left;
}
</style>
