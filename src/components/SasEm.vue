<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
      <v-flex xs12 md4 class="bodyCardAvatarQual">
        <br />
        <v-avatar size="130">
          <v-img src="../assets/item_logo/sas_logo.png" />
        </v-avatar>
        <br />
      </v-flex>
      <v-flex xs12 md8>
        <span class="bodyCardDateText">{{issuedDate}}</span>
        <br />
        <span class="bodyCardTitle">{{certName}}</span>
        <br />
        <p class="bodyCardText" v-for="detail in certDetail" :key="detail">{{detail}}</p>
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "SasEm",
  data: () => ({
    iconUrl: "sas_logo",
    certName: "SAS Certified Predictive Modeler Using SAS Enterprise Miner 14",
    issuedOrg: "SAS Institute Incorporation",
    issuedDate: "Jan 2019",
    expiredDate: null,
    certDetail: [
      "Issued by SAS Institute Incorporation",
      "Prepare data, build predictive models, assess and implement models and perform pattern analysis",
    ],
  }),
};
</script>
