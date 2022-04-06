<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
      <v-flex xs12 md3 class="bodyCardAvatarEdu">
        <br />
        <v-avatar size="130">
          <v-img src="../assets/item_logo/cityu_logo.png" />
        </v-avatar>
        <br />
      </v-flex>
      <v-flex xs12 md9>
        <span class="bodyCardDateText">{{bngPeriod}} - {{endPeriod}}</span>
        <br />
        <span class="bodyCardTitle">{{ programName }}, {{ schoolName }}</span>
        <br />
        <p class="bodyCardText">{{programDesp}}</p>
        <v-expansion-panels v-model="panel" multiple>
          <v-expansion-panel v-for="progDetail in programDetail" :key="progDetail.key">
            <v-expansion-panel-header>{{progDetail.sectionTitle}}</v-expansion-panel-header>
            <v-expansion-panel-content>
              <p class="bodyCardText">{{progDetail.sectionDept}}</p>
              <span
                class="bodyCardText"
                v-for="course in progDetail.courseDetail"
                :key="course.key"
              >
                {{course.courseCode}} {{course.courseTitle}} ({{course.courseGrade}})
                <br />
              </span>
            </v-expansion-panel-content>
          </v-expansion-panel>
        </v-expansion-panels>

        <!--
        <v-card v-for="detail in programDetail" :key="detail.key">
          <v-card-title>{{detail.sectionTitle}}</v-card-title>
          <span class="bodyCardText" v-for="course in detail.courseDetail" :key="course.key">
            {{course.courseCode}} {{course.courseTitle}} ({{course.courseGrade}})
            <br />
          </span>
        </v-card>
        -->
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "Cityu",
  data: () => ({
    schoolName: "City University of Hong Kong",
    iconUrl: "cityu_logo",
    bngPeriod: "Sep 2015",
    endPeriod: "Jul 2019",
    programName: "Bachelor of Business Administration",
    programDesp: "Second Class Honours, Upper Division (CGPA: 3.22/4.3)",
    programDetail: [
      {
        key: 1,
        sectionTitle: "Major in Business Analysis",
        sectionDept: "Department of Management Science",
        courseDetail: [
          {
            key: 1,
            courseCode: "MS4252",
            courseTitle: "Big Data Analytics",
            courseGrade: "A",
          },
          {
            key: 2,
            courseCode: "CB2022",
            courseTitle: "Business Programming with Spreadsheet",
            courseGrade: "A",
          },
          {
            key: 3,
            courseCode: "CB2200",
            courseTitle: "Business Statistics",
            courseGrade: "A",
          },
          {
            key: 4,
            courseCode: "CB2011",
            courseTitle: "Solving Business Problems with Spreadsheet Modeling",
            courseGrade: "A-",
          },
          {
            key: 5,
            courseCode: "MS3111",
            courseTitle:
              "Quantitative Business Analysis with Visual Basic for Applications",
            courseGrade: "B+",
          },
          {
            key: 6,
            courseCode: "MS3252",
            courseTitle: "Regression Analysis",
            courseGrade: "B",
          },
          {
            key: 7,
            courseCode: "MS4212",
            courseTitle: "Predictive Analytics and Forecasting",
            courseGrade: "B-",
          },
          {
            key: 8,
            courseCode: "MS4109",
            courseTitle: "Project Management",
            courseGrade: "B-",
          },
        ],
      },
      {
        key: 2,
        sectionTitle: "Minor in Information Management for Financial Services",
        sectionDept: "Department of Information Systems",
        courseDetail: [
          {
            key: 1,
            courseCode: "IS3430",
            courseTitle: "System Analysis and Design",
            courseGrade: "A",
          },
          {
            key: 2,
            courseCode: "IS4834",
            courseTitle: "Business Intelligence and Analytics",
            courseGrade: "A-",
          },
          {
            key: 3,
            courseCode: "IS4537",
            courseTitle: "Information Systems Audit",
            courseGrade: "B",
          },
          {
            key: 4,
            courseCode: "IS3237",
            courseTitle: "Information Services for Business Organization",
            courseGrade: "B",
          },
        ],
      },
      {
        key: 3,
        sectionTitle: "Minor in Computing",
        sectionDept: "Department of Computer Science",
        courseDetail: [
          {
            key: 1,
            courseCode: "CS1102",
            courseTitle: "Introduction to Computer Studies",
            courseGrade: "B+",
          },
          {
            key: 2,
            courseCode: "CS2360",
            courseTitle: "Java Programming",
            courseGrade: "B+",
          },
          {
            key: 3,
            courseCode: "CS2115",
            courseTitle: "Computer Organization",
            courseGrade: "B",
          },
          {
            key: 4,
            courseCode: "CS2204",
            courseTitle: "Fundamental of Internet Application Development",
            courseGrade: "B",
          },
        ],
      },
    ],
  }),
};
</script>
