<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
      <v-flex xs12 md4 class="bodyCardAvatarQual">
        <br />
        <v-avatar size="130">
          <v-img src="../assets/item_logo/coursera_logo.png" />
        </v-avatar>
        <br />
      </v-flex>
      <v-flex xs12 md8>
        <span class="bodyCardDateText">{{issuedDate}}</span>
        <br />
        <span class="bodyCardTitle">{{certName}}</span>
        <br />
        <p class="bodyCardText" v-for="detail in certDetail" :key="detail">{{detail}}</p>
        <ul>
          <li class="bodyCardTextList" v-for="course in courseList" :key="course">{{course}}</li>
        </ul>
        <br/>
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "PythonForEverybody",
  data: () => ({
    iconUrl: "coursera_logo",
    certName: "Python For Everybody Specialization",
    issuedOrg: "Coursera",
    issuedDate: "Jun 2021",
    expiredDate: null,
    certDetail: [
      "Issued by Coursera, partnered with University of Michigan",
      "Fundamental programming concepts including data structures, networked application program interfaces, and databases, using the Python programming language",
    ],
    courseList: [
      "Getting Started with Python",
      "Python Data Structures",
      "Using Python to Access Web Data",
      "Using Databases with Python",
      "Capstone: Retrieving, Processing, and Visualizing Data with Python",
    ]
  }),
};
</script>
