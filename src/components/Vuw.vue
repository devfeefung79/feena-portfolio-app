<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
      <v-flex xs12 md9>
        <span class="bodyCardDateText">{{bngPeriod}} - {{endPeriod}}</span>
        <br />
        <span class="bodyCardTitle">{{ programName }}, {{ schoolName }}</span>
        <br />
        <p class="bodyCardText">{{programDesp}}</p>
        <span class="bodyCardText" v-for="course in courseDetail" :key="course.key">
          {{course.courseCode}} {{course.courseTitle}} ({{course.courseGrade}})
          <br />
        </span>
      </v-flex>
      <v-flex xs12 md3 class="bodyCardAvatarEdu">
        <br />
        <v-avatar size="130">
          <v-img src="../assets/item_logo/vuw_logo.png" />
        </v-avatar>
        <br />
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "Vuw",
  data: () => ({
    schoolName: "Victoria University of Wellington",
    iconUrl: "vuw_logo",
    bngPeriod: "Jul 2017",
    endPeriod: "Nov 2017",
    programName: "Student Exchange Program",
    programDesp: "Faculty of Information Management",
    courseDetail: [
      {
        key: 1,
        courseCode: "INFO 151",
        courseTitle: "Datebases",
        courseGrade: "A+",
      },
      {
        key: 2,
        courseCode: "INFO 264",
        courseTitle: "Business Analytics",
        courseGrade: "B+",
      },
      {
        key: 3,
        courseCode: "MGMT 316",
        courseTitle: "Decision Modelling for Managers",
        courseGrade: "B+",
      },
      {
        key: 4,
        courseCode: "MARK 317",
        courseTitle: "Marketing Decision Support",
        courseGrade: "B",
      },
    ],
  }),
};
</script>
