<template>
  <v-card class="bodyCardContainer">
    <br />
    <span class="bodyCardTitle">Technical Skills</span>
    <br />
    <v-layout row wrap>
      <v-flex xs12 md4>
        <div v-for="skill in technial" :key="skill.key">
          <v-card class="skillCard" v-if="isFirstCol(skill.key)">
          <v-card-text>
          <v-chip class="skillChip" v-for="item in skill.items" :key="item.key">{{item}}</v-chip>
            </v-card-text>
        <v-card-title>{{ skill.category }}</v-card-title>
          </v-card>
        </div>
      </v-flex>
  <v-flex xs12 md4>
    <div v-for="skill in technial" :key="skill.key">
          <v-card class="skillCard" v-if="isSecondCol(skill.key)">
      <v-card-text>
      <v-chip class="skillChip" v-for="item in skill.items" :key="item.key">{{item}}</v-chip>
            </v-card-text>
    <v-card-title>{{ skill.category }}</v-card-title>
          </v-card>
        </div>
      </v-flex>
  <v-flex xs12 md4>
    <div v-for="skill in technial" :key="skill.key">
          <v-card class="skillCard" v-if="isThirdCol(skill.key)">
      <v-card-text>
      <v-chip class="skillChip" v-for="item in skill.items" :key="item.key">{{item}}</v-chip>
            </v-card-text>
    <v-card-title>{{ skill.category }}</v-card-title>
          </v-card>
        </div>
      </v-flex>
    </v-layout>
  </v-card>
</template>

  <script>
    export default {
      name: "TechnicalSkill",
  methods: {
      isFirstCol: function (toolKey) {
      if (toolKey % 3 == 1) {
        return true;
      } else return false;
    },
    isSecondCol: function (toolKey) {
      if (toolKey % 3 == 2) {
        return true;
      } else return false;
    },
    isThirdCol: function (toolKey) {
      if (toolKey % 3 == 0) {
        return true;
      } else return false;
    },
  },
  data: () => ({
      technial: [
      {
      key: 1,
        category: "Programming",
        items: [
          "Java",
          "JSP",
          "Spring",
          "SpringBoot",
          "Hibernate",
          "Python",
          "VBA",
          //"R",
          "SAS",
        ],
      },
      {
      key: 2,
        category: "Web Technology",
        items: [
          "HTML",
          "CSS",
          "LESS",
          "JavaScript",
          "TypeScript",
          "jQuery",
          "React",
          "Vue",
          "JSON",
          "REST API",
        ],
      },
      {
      key: 3,
        category: "Database",
        items: ["Oracle DB", "PostgreSQL", "MongoDB"],
      },
      /*
      {
      key: 6,
        category: "Software Testing",
        items: ["Selenium"],
      },
      */
    ],
  }),
};
</script>
