<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
      <v-flex xs12 md4 class="bodyCardAvatarQual">
        <br />
        <v-avatar size="130">
          <v-img src="../assets/item_logo/microsoft_logo.png" />
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
  name: "AzureData900",
  data: () => ({
    iconUrl: "microsoft_logo",
    certName: "Microsoft Certified Azure Data Fundamental",
    issuedOrg: "Microsoft Corporation",
    issuedDate: "Jul 2021",
    expiredDate: null,
    certDetail: [
      "Issued by Microsoft Corporation",
      "Demonstrate understanding of core data concepts, such as relational data, nonrelational data, big data, and analytics. Plus, familiarity with the roles, tasks, and responsibilities in the world of data and data analytics",
    ],
  }),
};
</script>
