<template>
  <v-card class="bodyCardContainer">
    <v-layout row wrap>
      <v-flex xs12 md7>
        <v-btn rounded class="projectLinkBtn" @click="openBonufoUrl()">
          <span>Live Demo</span>
        </v-btn>
         <v-btn rounded class="projectLinkBtn" @click="openBonufoSource()">
          <span>Source Code</span>
        </v-btn>
        <br/>
        <span class="bodyCardTitle">{{projectName}}</span>
        <br />
        <p class="bodyCardText">{{summary}}</p>
         <span class="bodyCardSubHeading">Functions:</span>
        <ul>
          <li class="bodyCardTextList" v-for="item in functionList" :key="item.key">{{item.label}}</li>
        </ul>
      </v-flex>
      <v-flex xs12 md5>
        <span class="bodyCardSubHeading">&emsp;</span>
        <v-carousel
            class="headerPic mb-5"
            height="240"
            cycle
            hide-delimiter-background
            show-arrows-on-hover
          >
          <v-carousel-item
            v-for="(item,i) in pictures"
            :key="i"
            :src="getItemPic(item.src)"
            reverse-transition="fade-transition"
            transition="fade-transition"
          ></v-carousel-item>
        </v-carousel>
        <span class="bodyCardSubHeading">Technologies used:</span>
        <v-chip class="techChip" v-for="tech in techStack" :key="tech.key">
          {{tech.label}}
        </v-chip>
        <br />
      </v-flex>
    </v-layout>
  </v-card>
</template>

<script>
export default {
  name: "ProjectBonufo",
  data: () => ({
    projectName: "English Writing Response Platform - BONUFO",
    techStack: [
      {
        key: 1,
        label: "React"
      },
      {
        key: 2,
        label: "TypeScript"
      },
      {
        key: 3,
        label: "HTML"
      },
      {
        key: 4,
        label: "CSS"
      },
      {
        key: 5,
        label: "Semantic UI"
      },
      {
        key: 6,
        label: "NodeJS"
      },
      {
        key: 7,
        label: "ExpressJS"
      },
      {
        key: 8,
        label: "JWT"
      },
      {
        key: 9,
        label: "MongoDB"
      }
      ],
    summary:
      "A platform to enhance English writing skill as a learner or give feedback to others' essay as a tutor",
    description:
      "Responsible for reviewing user requirements and transform it into functional components on cloud",
    functionList: [
      {
        key: 1,
        label: "Register for an account as a learner or a tutor"
      },
      {
        key: 2,
        label: "Search questions with criteria (keyword, topic, question type, related exam)"
      },
      {
        key: 3,
        label: "Write an essay responded to a question (Learner)"
      },
      {
        key: 4,
        label: "Choose a marking scheme for an essay for particular exam preparation, e.g. IELTS, CELPIP (Learner)"
      },
      {
        key: 5,
        label: "Give score and comment to an essay (Tutor)"
      },
      {
        key: 6,
        label: "View saved questions in profile page"
      },
       {
        key: 7,
        label: "View previous submission and the corresponding average score calculated (Learner)"
      },
    ],
    pictures: [
      {
        src: "screen1",
      },
      {
        src: "screen2",
      },
      {
        src: "screen3",
      },
      {
        src: "screen4",
      },
      {
        src: "screen5",
      },
      {
        src: "screen6",
      },
      {
        src: "screen7",
      },
      {
        src: "screen8",
      },
    ],
  }),
  methods: {
    getItemPic: function (filename) {
      var images = require.context("../assets/pic_bonufo/", false, /\.jpeg$/);
      return images("./" + filename + ".jpeg");
    },
    openBonufoUrl: function () {
      window.open(
        "https://bonufo-react.vercel.app",
        "_blank"
      );
    },
    openBonufoSource: function () {
      window.open(
        "https://github.com/devfeefung79/bonufo-react",
        "_blank"
      );
    },
  },
};
</script>
