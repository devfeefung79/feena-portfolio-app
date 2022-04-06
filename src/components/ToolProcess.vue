<template>
  <v-card class="bodyCardContainer">
    <br />
    <span class="bodyCardTitle">Tools & Processes</span>
    <br />
    <v-layout row wrap>
      <v-flex xs12 md6>
        <div v-for="skill in tool" :key="skill.key">
          <v-card class="skillCard" v-if="isFirstCol(skill.key)">
            <v-card-text>
              <v-chip class="skillChip" v-for="item in skill.items" :key="item.key">{{item}}</v-chip>
            </v-card-text>
            <v-card-title>{{skill.category}}</v-card-title>
          </v-card>
        </div>
      </v-flex>
      <v-flex xs12 md6>
        <div v-for="skill in tool" :key="skill.key">
          <v-card class="skillCard" v-if="isSecondCol(skill.key)">
            <v-card-text>
              <v-chip class="skillChip" v-for="item in skill.items" :key="item.key">{{item}}</v-chip>
            </v-card-text>
            <v-card-title>{{skill.category}}</v-card-title>
          </v-card>
        </div>
      </v-flex>
      <!--
      <v-col cols="4">
        <div v-for="skill in tool" :key="skill.key">
          <v-card class="skillCard" v-if="isThirdCol(skill.key)">
            <v-card-text>
              <v-chip class="skillChip" v-for="item in skill.items" :key="item.key">{{item}}</v-chip>
            </v-card-text>
            <v-card-title>{{skill.category}}</v-card-title>
          </v-card>
        </div>
      </v-col>
      -->
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "ToolProcess",
  methods: {
    isFirstCol: function (toolKey) {
      if (toolKey % 2 == 0) {
        return true;
      } else return false;
    },
    isSecondCol: function (toolKey) {
      if (toolKey % 2 == 1) {
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
    tool: [
      {
        key: 1,
        category: "Data Analysis",
        items: ["SAS 9.4", "SAS EM", "Tableau"],
      },
      {
        key: 3,
        category: "System Analysis",
        items: ["UML", "MS Visio"],
      },
      {
        key: 2,
        category: "Project Management",
        items: ["SDLC", "Scrum", "Agile", "MS Project"],
      },
      /*{
        key: 6,
        category: "Service Management",
        items: ["ITIL"],
      },
      */
     {
        key: 4,
        category: "Data Processing",
        items: ["Informatica"],
      },
      {
        key: 6,
        category: "Cloud Technology",
        items: ["Azure", "AWS"],
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
