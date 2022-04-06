<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
      <v-flex xs12 md9>
        <span class="bodyCardDateText">{{bngPeriod}} - {{endPeriod}}</span>
        <br />
        <span class="bodyCardTitle">{{jobTitle}} in {{companyName}}</span>
        <br />
        <p class="bodyCardText">{{jobDuty}}</p>
        <p class="bodyCardText">{{jobDetail}}</p>
      </v-flex>
      <v-flex xs12 md3 class="bodyCardAvatarWorkExp">
        <br />
        <v-avatar size="130">
          <v-img src="../assets/item_logo/ibm_logo.png" />
        </v-avatar>
        <br />
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "Ibm",
  data: () => ({
    companyName: "IBM",
    iconUrl: "ibm_logo",
    location: "Hong Kong",
    bngPeriod: "Feb 2021",
    endPeriod: "Feb 2022",
    jobTitle: "Analyst Programmer",
    jobDuty:
      "Develop data warehouse and ETL solutions with AWS and Informatica",
    jobDetail:
      "Responsible for reviewing user requirements and transform it into functional components on cloud",
  }),
};
</script>
