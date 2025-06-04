<template>
  <div id="container">
    <div id="info">
      <h2>Info</h2>
      <p>이름 : {{ name }}</p>
      <p>생년 월일 : {{ birthday }}</p>
      <p v-if="army.isMilitaryService">
        군 복무 : {{ army.branch }} - {{ army.role }}({{ army.period.start }} ~
        {{ army.period.end }})
      </p>
    </div>

    <div id="skill">
      <h2>Skill</h2>
      <p>{{ backend }}</p>
      <p>{{ front }}</p>
      <p>{{ devOps }}</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "ContactMe",

  data() {
    return {
      name: "한만욱",
      birthday: "1999.07.07",
      army: {
        isMilitaryService: true,
        branch: "공군",
        role: "fire",
        period: {
          start: "2022.09",
          end: "2024.06",
        },
      },
      backend: null,
      front: ["react", "vue", "git", "wiki", "jira"].join(","),
      devOps: null,
    };
  },

  created() {
    this.front = ["VueJs", "React"].join(",");
  },

  mounted() {
    this.devOps = ["Git", "WIKI", "Jira"].join(",");
  },
};
</script>

<style scoped>
#container {
  display: flex;
  border-bottom: 1px solid gray;
  margin-bottom: 10px;
  min-height: 100%;
}
div {
  text-align: left;
}

#info {
  width: 50%;
  padding: 10px;
}

#skill {
  width: 50%;
  padding: 10px;
}

a {
  text-decoration: none;
}
</style>
