<template>
  <div>
    <h2>학교</h2>

    <p v-for="edu in eduList" :key="edu.name">
      {{ edu.name }} {{ edu.type }}({{ edu.start }} ~
      {{ edu.end ? edu.end : "재학 중" }})
    </p>
  </div>
</template>

<script>
export default {
  name: "EducationList",
  data() {
    return {
      eduList: [
        {
          name: "인하초등학교",
          type: "졸업",
          start: "1999.03",
          end: "2006.02",
        },
        { name: "인하중학교", type: "졸업", start: "2006.03", end: "2009.02" },
        {
          name: "인하고등학교",
          type: "졸업",
          start: "2009.03",
          end: "2012.02",
        },
        { name: "인하대학교", type: "재학", start: "2012.03", end: null },
      ],
    };
  },
};
</script>

<style scoped>
div {
  text-align: left;
  border-bottom: 1px solid gray;
}
</style>
