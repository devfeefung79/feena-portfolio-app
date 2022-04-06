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
          <v-img src="../assets/item_logo/microsoft_logo.png" />
        </v-avatar>
        <br />
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "AzureAi900",
  data: () => ({
    iconUrl: "microsoft_logo",
    certName: "Microsoft Certified Azure AI Fundamental",
    issuedOrg: "Microsoft Corporation",
    issuedDate: "Jun 2021",
    expiredDate: null,
    certDetail: [
      "Issued by Microsoft Corporation",
      "Demonstrate foundational knowledge of machine learning and AI concepts, along with related Azure services",
    ],
  }),
};
</script>
