<template>
  <v-card class="bodyCardContainer">
    <span class="bodyCardTitle">Technical Skills</span>
    <br />
    <br />
    <v-layout row wrap>
      <v-flex xs12 md6>
        <div v-for="skill in tool" :key="skill.key">
          <v-card class="skillCard" v-if="isFirstCol(skill.key)">
            <v-card-text>
              <v-chip class="techChip" v-for="item in skill.items" :key="item.key">{{item}}</v-chip>
            </v-card-text>
            <v-card-title>{{skill.category}}</v-card-title>
          </v-card>
        </div>
      </v-flex>
      <v-flex xs12 md6>
        <div v-for="skill in tool" :key="skill.key">
          <v-card class="skillCard" v-if="isSecondCol(skill.key)">
            <v-card-text>
              <v-chip class="skillChipOne" v-for="item in skill.items" :key="item.key">{{item}}</v-chip>
            </v-card-text>
            <v-card-title>{{skill.category}}</v-card-title>
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
      if (toolKey % 2 == 1) {
        return true;
      } else return false;
    },
    isSecondCol: function (toolKey) {
      if (toolKey % 2 == 0) {
        return true;
      } else return false;
    }
  },
  data: () => ({
    tool: [
      {
      key: 1,
        category: "Web Development",
        items: [
          "JavaScript",
          "TypeScript",
          "React",
          "NodeJS",
          "Vue",
          "HTML",
          "CSS",
          "LESS",
          "SCSS",
          "JSON",
          "REST API",
          "jQuery"
        ],
      },
      {
      key: 2,
        category: "Software Development",
        items: [
          "Java",
          "SpringBoot",
          "Hibernate",
          "Python"
        ],
      },
      {
      key: 3,
        category: "Database",
        items: ["Oracle DB", "PostgreSQL", "MongoDB"],
      },
      {
        key: 5,
        category: "Cloud Technology",
        items: ["Azure", "AWS"],
      },
      {
        key: 4,
        category: "Data Analysis",
        items: ["SAS", "Tableau", "Informatica", "VBA"],
      },
      {
        key: 6,
        category: "Tool & Process",
        items: ["SDLC", "Agile", "UML", "Git", "MS Visio", "MS Project"],
      },
      /*{
        key: 4,
        category: "CI/CD",
        items: ["Git", "Docker", "Jenkins"],
      },
      */
    ],
  }),
};
</script>
