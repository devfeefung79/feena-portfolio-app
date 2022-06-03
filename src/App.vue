<template>
  <v-app class="baseContainer">
    <!-- Top Button List -->
    <v-card id="topCard" class="topCard text-right">
      <v-btn rounded class="linkBtn" @click="openGitHubProfile()">
        <v-icon size="large">mdi-github</v-icon>
        <span>GitHub</span>
      </v-btn>
      <v-btn rounded class="linkBtn" @click="openLinkedProfile()">
        <v-icon size="large">mdi-linkedin</v-icon>
        <span>Linkedin</span>
      </v-btn>
      <v-btn rounded class="linkBtn" @click="sendEmail()">
        <v-icon size="large">mdi-email</v-icon>
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
            height="300"
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
      <a href="#projectSection">
        <v-avatar>
          <span class="sidebar-link-text">Project</span>
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
      <v-card class="sectionContentCardFirstCenter">
        <AboutMe />
      </v-card>

      <v-card class="sectionTitleCard" id="projectSection">Project</v-card>

      <v-card class="sectionContentCardCenter">
        <ProjectBonufo />
      </v-card>

      <v-card class="sectionTitleCard" id="workExpSection">Work Experience</v-card>

      <v-card class="sectionContentCardCenter">
        <Ibm />
      </v-card>

      <v-card class="sectionContentCardCenter">
        <DxcTech />
      </v-card>

      <v-card class="sectionContentCardCenter">
        <PccwSolu />
      </v-card>

      <v-card class="sectionContentCardCenter">
        <Clp />
      </v-card>

      <v-card class="sectionTitleCard" id="skillSection">Skills & Abilities</v-card>
      <!--
      <v-card class="sectionContentCard">
        <TechnicalSkill />
      </v-card>
      -->

      <v-layout row wrap class="sectionContentCardFirstCenter">
        <v-flex xs12 md8>
          <v-card class="sectionContentCard scratchCard">
            <TechnicalSkill />
          </v-card>
        </v-flex>
        <v-flex xs12 md4>
          <LanguageSkill />
        </v-flex>
      </v-layout>

      <v-card class="sectionTitleCard" id="eduSection">Education</v-card>
      <v-card class="sectionContentCardCenter">
        <Cityu />
      </v-card>

      <v-card class="sectionContentCardCenter">
        <Vuw />
      </v-card>

      <v-card class="sectionTitleCard" id="qualSection">Qualifications</v-card>
      <v-card class="sectionContentCardCenter">
        <AwsSolutionAsso />
      </v-card>

      <v-card class="sectionContentCardCenter">
        <IbmDataScience />
      </v-card>
      
      <v-card class="sectionContentCardCenter">
        <AzureData900 />
      </v-card>

      <v-card class="sectionContentCardCenter">
        <AzureAi900 />
      </v-card>

      <v-card class="sectionContentCardCenter">
        <PythonForEverybody />
      </v-card>

      <v-card class="sectionContentCardCenter">
        <Azure900 />
      </v-card>

      <v-card class="sectionContentCardCenter">
        <SasEm />
      </v-card>

      <v-card class="sectionContentCardCenter">
        <DevOps200 />
      </v-card>

      <v-card class="sectionContentCardCenter">
        <SasProg />
      </v-card>
    </v-content>

    <!-- Page Footer -->
    <v-card class="footerCard">© 2022 Feena Fung. All rights reserved.</v-card>
  </v-app>
</template>

<script>
import AboutMe from "./components/AboutMe";
import ProjectBonufo from "./components/ProjectBonufo";
import Ibm from "./components/Ibm";
import DxcTech from "./components/DxcTech";
import PccwSolu from "./components/PccwSolu";
import Clp from "./components/Clp";
import LanguageSkill from "./components/LanguageSkill";
import TechnicalSkill from "./components/TechnicalSkill";
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
    ProjectBonufo,
    Ibm,
    DxcTech,
    PccwSolu,
    Clp,
    Cityu,
    Vuw,
    LanguageSkill,
    TechnicalSkill,
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
      "Dedicated full-stack developer with 3 years of experience in IT industry with academic background in computing, information systems, data science and statistics. Skills include web development with React, Java & JavaScript programming, SQL, systems analysis and design, cloud computing in AWS & Azure. Easy-going, unflappable, eager to learn and love to take challenges.",
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
        "https://www.linkedin.com/in/feena-fung/",
        "_blank"
      );
    },
    openGitHubProfile: function () {
      window.open(
        "https://github.com/devfeefung79",
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
