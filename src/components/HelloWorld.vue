<template>
  <div id="app">
    <NameCard />
    <AboutMe />
    <Info />
    <Contact />
    <Education />
    <Project />
    <FamilyInfo />
  </div>
</template>

<script>
// 포트폴리오 제목 컴포넌트
import NameCard from "./NameCard.vue";
// 자기 소개 컴포넌트
import AboutMe from "./AboutMe.vue";
// 정보 컴포넌트
import Info from "./Info.vue";
// 연락처 컴포넌트
import Contact from "./Contact.vue";
// 학교 정보 컴포넌트
import Education from "./Education.vue";
// 프로젝트 컴포넌트
import Project from "./Project.vue";

import FamilyInfo from "./FamilyInfo.vue";

export default {
  name: "App",
  components: {
    NameCard,
    Info,
    Contact,
    AboutMe,
    Education,
    Project,
    FamilyInfo,
  },
};
</script>

<style>
#app {
  max-width: 80%;
  margin: 60px auto;

  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

h1,
h2,
p {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
}

li {
  margin: 10;
}
</style>
