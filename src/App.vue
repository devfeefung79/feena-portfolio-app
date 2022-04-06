<template>
  <v-app class="baseContainer">
    <!-- Top Button List -->
    <v-card id="topCard" class="topCard text-right">
      <!-- Resume
      <v-btn rounded class="linkBtn">
        <v-icon size="small">mdi-file</v-icon>
        <span>Resume</span>
      </v-btn>
      -->
      <v-btn rounded class="linkBtn" @click="openLinkedProfile()">
        <v-icon size="small">mdi-linkedin</v-icon>
        <span>Linkedin</span>
      </v-btn>
      <v-btn rounded class="linkBtn" @click="sendEmail()">
        <v-icon size="small">mdi-email</v-icon>
        <span>Email</span>
      </v-btn>
    </v-card>

    <!-- Scroll To Top Icon -->
    <a href="#topCard">
      <v-icon class="scrollUpIcon">mdi-arrow-up-thick</v-icon>
    </a>

    <!-- Page Title Card -->
    <v-card class="headerCard">
      <v-layout row wrap>
        <v-flex xs12 md8 class="text-left">
          <br/>
          <div class="headerTitleBlock">
            <h1 class="headerTitle">{{headerTitle}}</h1>
            <span class="headerText">{{summaryText}}</span>
          </div>
        </v-flex>
        <v-flex xs12 md4 class="headerPicCol">
          <v-carousel
            class="headerPic"
            height="320"
            cycle
            hide-delimiter-background
            show-arrows-on-hover
          >
            <v-carousel-item
              v-for="(item,i) in items"
              :key="i"
              :src="getItemPic(item.src)"
              reverse-transition="fade-transition"
              transition="fade-transition"
            ></v-carousel-item>
          </v-carousel>
        </v-flex>
      </v-layout>
    </v-card>

    <!-- Side Bar -->
    <div id="menu">
      <a href="#aboutMeSection">
        <v-avatar>
          <span class="sidebar-link-text">About</span>
        </v-avatar>
      </a>
      <br />
      <a href="#workExpSection">
        <v-avatar>
          <span class="sidebar-link-text">Experience</span>
        </v-avatar>
      </a>
      <br />
      <a href="#skillSection">
        <v-avatar>
          <span class="sidebar-link-text">Skill</span>
        </v-avatar>
      </a>
      <br />
      <a href="#eduSection">
        <v-avatar>
          <span class="sidebar-link-text">Education</span>
        </v-avatar>
      </a>
      <br />
      <a href="#qualSection">
        <v-avatar>
          <span class="sidebar-link-text">Qualification</span>
        </v-avatar>
      </a>
    </div>

    <!-- Page Content -->
    <v-content class="bodyContainer">
      <v-card class="sectionTitleCardFirst" id="aboutMeSection">About Me</v-card>
      <AboutMe />

      <v-card class="sectionTitleCard" id="workExpSection">Work Experience</v-card>

      <v-card class="sectionContentCard">
        <Ibm />
      </v-card>

      <v-card class="sectionContentCard">
        <DxcTech />
      </v-card>

      <v-card class="sectionContentCard">
        <PccwSolu />
      </v-card>

      <v-card class="sectionContentCard">
        <Clp />
      </v-card>

      <v-card class="sectionTitleCard" id="skillSection">Skills & Abilities</v-card>
      <v-card class="sectionContentCard">
        <TechnicalSkill />
      </v-card>

      <v-layout row wrap>
        <v-flex xs12 md5>
          <LanguageSkill />
        </v-flex>
        <v-flex xs12 md7>
          <v-card class="sectionContentCard scratchCard">
            <ToolProcess />
          </v-card>
        </v-flex>
      </v-layout>

      <v-card class="sectionTitleCard" id="eduSection">Education</v-card>
      <v-card class="sectionContentCard">
        <Cityu />
      </v-card>

      <v-card class="sectionContentCard">
        <Vuw />
      </v-card>

      <v-card class="sectionTitleCard" id="qualSection">Qualification</v-card>
      <v-card class="sectionContentCard">
        <AwsSolutionAsso />
      </v-card>

      <v-card class="sectionContentCard">
        <IbmDataScience />
      </v-card>
      
      <v-card class="sectionContentCard">
        <AzureData900 />
      </v-card>

      <v-card class="sectionContentCard">
        <AzureAi900 />
      </v-card>

      <v-card class="sectionContentCard">
        <PythonForEverybody />
      </v-card>

      <v-card class="sectionContentCard">
        <Azure900 />
      </v-card>

      <v-card class="sectionContentCard">
        <SasEm />
      </v-card>

      <v-card class="sectionContentCard">
        <DevOps200 />
      </v-card>

      <v-card class="sectionContentCard">
        <SasProg />
      </v-card>
    </v-content>

    <!-- Page Footer -->
    <v-card class="footerCard">© 2022 Feena Fung. All rights reserved.</v-card>
  </v-app>
</template>

<script>
import AboutMe from "./components/AboutMe";
import Ibm from "./components/Ibm";
import DxcTech from "./components/DxcTech";
import PccwSolu from "./components/PccwSolu";
import Clp from "./components/Clp";
import LanguageSkill from "./components/LanguageSkill";
import TechnicalSkill from "./components/TechnicalSkill";
import ToolProcess from "./components/ToolProcess";
import Cityu from "./components/Cityu";
import Vuw from "./components/Vuw";
import IbmDataScience from "./components/IbmDataScience";
import AzureAi900 from "./components/AzureAi900";
import Azure900 from "./components/Azure900";
import PythonForEverybody from "./components/PythonForEverybody";
import AzureData900 from "./components/AzureData900";
import AwsSolutionAsso from "./components/AwsSolutionAsso";
import SasEm from "./components/SasEm";
import DevOps200 from "./components/DevOps200";
import SasProg from "./components/SasProg";

export default {
  name: "App",
  components: {
    AboutMe,
    Ibm,
    DxcTech,
    PccwSolu,
    Clp,
    Cityu,
    Vuw,
    LanguageSkill,
    TechnicalSkill,
    ToolProcess,
    PythonForEverybody,
    AzureData900,
    AwsSolutionAsso,
    IbmDataScience,
    AzureAi900,
    Azure900,
    DevOps200,
    SasEm,
    SasProg
  },
  data: () => ({
    headerTitle: "FUNG, Tsz Ling (Feena)",
    headerSubTitle: "Full Stack Programmer",
    summaryTitle: "Full Stack Programmer",
    summaryText:
      "Dedicated developer with more than 2 years of experience in IT industry. I engaged in web application development with modern framework including React, Vue, Spring and data warehouse solution development with ETL and cloud solutions. I am passionate about system analysis and software development and eager to exlore new technologies.",
    emailAddress: "feenafungftl@gmail.com",
    items: [
      {
        src: "08022020_pic1",
      },
      {
        src: "08022020_pic2",
      },
      {
        src: "08022020_pic7",
      },
      {
        src: "08022020_pic6",
      },
    ],
  }),
  methods: {
    getItemPic: function (filename) {
      var images = require.context("./assets/pic_feena/", false, /\.jpeg$/);
      return images("./" + filename + ".jpeg");
    },
    openLinkedProfile: function () {
      window.open(
        "https://www.linkedin.com/in/feena-tsz-ling-fung-b55019136",
        "_blank"
      );
    },
    sendEmail: function () {
      var link = "mailto:feenafungftl@gmail.com";
      window.location.href = link;
    },
  },
};
</script>
