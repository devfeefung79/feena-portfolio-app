<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
      <v-flex xs12 md3 class="bodyCardAvatarWorkExp">
        <br />
        <v-avatar size="130">
          <v-img src="../assets/item_logo/clp_logo.png" />
        </v-avatar>
      </v-flex>
      <v-flex xs12 md9>
        <span class="bodyCardDateText">{{bngPeriod}} - {{endPeriod}}</span>
        <br />
        <span class="bodyCardTitle">{{jobTitle}} in {{companyName}}</span>
        <br />
        <p class="bodyCardText">{{jobDuty}}</p>
        <p class="bodyCardText">{{jobDetail}}</p>
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "Clp",
  data: () => ({
    companyName: "CLP Power Hong Kong Limited",
    iconUrl: "clp_logo",
    location: "Hong Kong",
    bngPeriod: "Jun 2018",
    endPeriod: "Feb 2019",
    jobTitle: "IT Intern",
    jobDuty:
      "Engaging in application development and support for enterprise solutions",
    jobDetail:
      "Responsible for data warehousing using MSSQL, preparing test automation script on cloud application and supporting documentation such as functional specification, testing log",
  }),
};
</script>
