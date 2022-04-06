<template>
  <div class="langBodyContainer">
    <v-card class="engSkillCard">
      <span class="bodyCardTitle">English Proficiency</span>
      <p class="bodyCardText">CEFR B2 User (Upper Intermediate)</p>
      <v-expansion-panels class="engSkillExpand" v-model="panel" multiple>
        <v-expansion-panel>
          <v-expansion-panel-header>IELTS Academic (29/2/2020)</v-expansion-panel-header>
          <v-expansion-panel-content>
            <span class="bodyCardText">Reading: 6.5/9</span>
            <br />
            <span class="bodyCardText">Writing: 6.5/9</span>
            <br />
            <span class="bodyCardText">Listening: 7.0/9</span>
            <br />
            <span class="bodyCardText">Speaking: 6.0/9</span>
            <br />
            <span class="bodyCardText">Overall: 6.5/9</span>
          </v-expansion-panel-content>
        </v-expansion-panel>
        <v-expansion-panel>
          <v-expansion-panel-header>TOEIC (27/10/2019)</v-expansion-panel-header>
          <v-expansion-panel-content>
            <span class="bodyCardText">Reading: 455/495</span>
            <br />
            <span class="bodyCardText">Writing: 180/200</span>
            <br />
            <span class="bodyCardText">Listening: 465/495</span>
            <br />
            <span class="bodyCardText">Speaking: 140/200</span>
          </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-card>
    <v-card class="chiSkillCard">
      <span class="bodyCardTitle">Chinese Proficiency</span>
      <p class="bodyCardText">Cantonese Native Speaker</p>
      <p class="bodyCardText">Mandarin Advanced User</p>
    </v-card>
  </div>
</template>

<script>
export default {
  name: "LanguageSkill",
};
</script>
