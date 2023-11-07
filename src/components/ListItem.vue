<template>
  <div class="list-item">
    <button @click="toggleActive" :class="{ 'active': isActive }">{{ item.name }}</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isActive: false,
    };
  },
  props: {
    item: {
      type: Object,
      required: true,
    },
  },
  methods: {
    toggleActive() {
      this.isActive = !this.isActive;
    },
  },
};
</script>