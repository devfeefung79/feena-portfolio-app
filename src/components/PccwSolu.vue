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
          <v-img src="../assets/item_logo/pccw_solutions_logo.png" />
        </v-avatar>
        <br />
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "PccwSolu",
  data: () => ({
    companyName: "PCCW Solutions. Ltd",
    iconUrl: "pccw_solutions_logo",
    location: "Hong Kong",
    bngPeriod: "Aug 2019",
    endPeriod: "May 2020",
    jobTitle: "ICT Graduate Trainee",
    jobDuty:
      "Engaging in frontend web development for an enterprise application using React JS and Typescript",
    jobDetail:
      "Responsible for reviewing UI design technical feasibility with Business Analysts and handling RESTful API in JSON format ",
  }),
};
</script>
