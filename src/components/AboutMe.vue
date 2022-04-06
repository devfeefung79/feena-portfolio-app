<template>
  <div class="aboutMeBodyContainer">
    <v-layout row wrap>
      <v-flex xs12 md6 class="aboutMeFlex">
        <v-card class="aboutMeCard">
          <br />
          <v-avatar size="150">
            <v-img src="../assets/picture/coffee.jpg" />
          </v-avatar>
          <br />
          <br />
          <span class="bodyCardTitle">{{leftContent.title}}</span>
          <p class="bodyCardText">{{leftContent.text}}</p>
        </v-card>
      </v-flex>
      <v-flex xs12 md6 class="aboutMeFlex">
        <v-card class="aboutMeCard">
          <br />
          <v-avatar size="150">
            <v-img src="../assets/picture/work.jpeg" />
          </v-avatar>
          <br />
          <br />
          <span class="bodyCardTitle">{{rightContent.title}}</span>
          <p class="bodyCardText">{{rightContent.text}}</p>
        </v-card>
        </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
  name: "AboutMe",
  methods: {
    getItemLogo: function (filename) {
      var images = require.context("../assets/item_logo/", false, /\.png$/);
      return images("./" + filename + ".png");
    },
  },
  data: () => ({
    leftContent: {
      title: "My Life",
      text:
        "A morning coffee is my energy for the day! I love solving puzzles, watching movie and planning for my future. Also, I enjoy hiking and chatting with my friends and family on weekend.",
    },
    rightContent: {
      title: "My Aspiration",
      text:
        "It is fulfilling to develop software solutions that bring values to others with my expertise. I like to study IT knowledge and new technologies continually, so as to enhance my technical abilities and make great contributions in my career.",
    },
  }),
};
</script>
