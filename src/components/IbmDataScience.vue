<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
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
      <v-flex xs12 md4 class="bodyCardAvatarQual">
        <br />
        <v-avatar size="130">
          <v-img src="../assets/item_logo/coursera_logo.png" />
        </v-avatar>
        <br />
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "IbmDataScience",
  data: () => ({
    iconUrl: "coursera_logo",
    certName: "IBM Data Science",
    issuedOrg: "Coursera",
    issuedDate: "Nov 2021",
    expiredDate: null,
    certDetail: [
      "Issued by Coursera, partnered with IBM Skills Network",
      "With an orientation of Data Science and its Methodology, became familiar and used a variety of data science tools, learned Python and SQL, performed Data Visualization and Analysis, and created Machine Learning models.",
    ],
    courseList: [
      "What is Data Science?",
      "Tools for Data Science",
      "Data Science Methodology",
      "Python for Data Science, AI & Development",
      "Python Project for Data Science",
      "Databases and SQL for Data Science with Python",
      "Data Analysis with Python",
      "Data Visualization with Python",
      "Machine Learning with Python",
      "Applied Data Science Capstone",
    ]
  }),
};
</script>
