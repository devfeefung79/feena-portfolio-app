<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
      <v-flex xs12 md8>
        <span class="bodyCardDateText">{{issuedDate}}</span>
        <br />
        <span class="bodyCardTitle">{{certName}}</span>
        <br />
        <p class="bodyCardText" v-for="detail in certDetail" :key="detail">{{detail}}</p>
      </v-flex>
      <v-flex xs12 md4 class="bodyCardAvatarQual">
        <br />
        <v-avatar size="130">
          <v-img src="../assets/item_logo/edx_logo.jpg" />
        </v-avatar>
        <br />
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "DevOps200",
  data: () => ({
    iconUrl: "edx_logo",
    certName: "DevOps200.3x: Continuous Integration and Continuous Deployment",
    issuedOrg: "Edx",
    issuedDate: "Dec 2018",
    expiredDate: null,
    certDetail: [
      "Issued by Edx, partnered with Microsoft Corporation",
      "Implement the DevOps practices of CI/CD with Azure DevOps Server and Microsoft Azure",
    ],
  }),
};
</script>
