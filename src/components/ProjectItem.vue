<template>
  <div>
    <h3>{{ project.title }}</h3>
    <ul>
      <li v-for="(item, index) in project.items" :key="index">{{ item }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ProjectItem",
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
};
</script>

<style scoped></style>
