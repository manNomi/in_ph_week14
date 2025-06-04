<template>
  <div id="container">
    <div id="family">
      <h2>Family</h2>
      <div
        v-for="member in familyMembers"
        :key="member.id"
        class="family-member"
        @mouseenter="hoveredMember = member.id"
        @mouseleave="hoveredMember = null">
        <p>
          {{ member.name }} - {{ member.relation }} :
          {{ hoveredMember === member.id ? member.fullSSN : member.maskedSSN }}
        </p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "FamilyInfo",
  data() {
    return {
      hoveredMember: null,
      familyMembers: [
        {
          id: 1,
          name: "김아빠",
          relation: "Father",
          fullSSN: "810101-1234567",
          maskedSSN: "810101-*******",
        },
        {
          id: 2,
          name: "김엄마",
          relation: "Mother",
          fullSSN: "820202-2345678",
          maskedSSN: "820202-*******",
        },
        {
          id: 3,
          name: "김철수",
          relation: "Son",
          fullSSN: "040403-3456789",
          maskedSSN: "040403-*******",
        },
        {
          id: 4,
          name: "김영희",
          relation: "Daughter",
          fullSSN: "050504-4567890",
          maskedSSN: "050504-*******",
        },
      ],
    };
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

#family {
  width: 100%;
  padding: 10px;
}

.family-member {
  cursor: pointer;
}
</style>
