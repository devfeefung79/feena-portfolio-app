<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
      <v-flex xs12 md3 class="bodyCardAvatarWorkExp">
        <br />
        <v-avatar size="130">
          <v-img src="../assets/item_logo/dxc_tech_logo.png" />
        </v-avatar>
        <br />
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
  name: "DxcTech",
  data: () => ({
    companyName: "DXC Technology Ltd.",
    iconUrl: "dxc_tech_logo",
    location: "Hong Kong",
    bngPeriod: "May 2020",
    endPeriod: "Feb 2021",
    jobTitle: "Programmer",
    jobDuty:
      "Engaging in J2EE application development using Spring, Hibernate, Oracle DBMS",
    jobDetail:
      "Responsible for developing technical specification and implementations of Java application including database design, unit test, functional test",
  }),
};
</script>
