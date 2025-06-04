<template>
  <div id="container">
    <h2>Project</h2>
    <ProjectItem
      v-for="(item, index) in projects"
      :key="index"
      :project="item" />
  </div>
  <div />
</template>

<script>
// ProjectItem.vue 컴포넌트를 import합니다.
import ProjectItem from "./ProjectItem.vue";

export default {
  name: "ProjectList",
  components: {
    ProjectItem,
  },
  data() {
    return {
      projects: [
        {
          title: "XXX 배달 프로젝트",
          items: [
            "Spring, React 기반 배달 앱 프로젝트",
            "일평균 5000건 주문",
            "마이크로 서비스 아키텍처, 아파치 카프카를 통한 시스템 설계",
          ],
        },
        {
          title: "XXX 배달 음식 추천 프로젝트",
          items: [
            "XXX 배달 앱에서 머신런닝을 활용한 배달 음식 추천",
            "사용자의 취향을 고려한 배달 음식 추천 알고리즘 설계",
          ],
        },
        {
          title: "XXX 배달 라이더 매칭 프로젝트",
          items: [
            "위치기반 배달 라이더 매칭 시스템 개발",
            "음식 종류에 따라 오토바이, 뚜벅이 라이더 자동 매칭 알고리즘 설계",
          ],
        },
      ],
    };
  },
};
</script>

<style scoped>
#container {
  border-bottom: 1px solid gray;
}

div {
  text-align: left;
}
</style>
