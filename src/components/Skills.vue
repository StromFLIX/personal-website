<template>
  <div class="skills">
    <v-card max-width="374" class="ma-7" v-for="(item, i) in items" :key="i">
      <v-card-title>{{item.skill}}</v-card-title>
      <v-card-text>
        <v-row align="center" class="mx-0">
          <v-rating :value="item.skilllevel" color="amber" dense half-increments readonly size="14"></v-rating>
        </v-row>
        <div>{{item.description}}</div>
      </v-card-text>

      <v-divider class="mx-4"></v-divider>

      <v-card-text>
        <v-chip-group v-model="selection" active-class="deep-purple accent-4 white--text" column >
          <v-chip v-for="(subskill, j) in item.subskills" :key="j">{{subskill}}</v-chip>
        </v-chip-group>
      </v-card-text>
    </v-card>
  </div>
</template>
<script>
export default {
  data: () => ({
    items: [
      {
        skill: "Amazon Web Services",
        skilllevel: 4,
        description:
          "Knowledge in all important areas of AWS, for example in EC2, Route 53 and S3",
        subskills: [
          "EC2",
          "IAM",
          "Lambda",
          "S3",
          "Code Pipeline",
          "Route 53",
          "Elastic Search",
          "DynamoDB"
        ]
      },
      {
        skill: "Docker",
        skilllevel: 4,
        description:
          "Heavy use of docker and docker-compose in past development Applications",
        subskills: [
          "Docker",
          "Docker-compose",
          "Docker networking",
          "Docker stack",
          "Docker secrets"
        ]
      },
      {
        skill: "Node.js",
        skilllevel: 5,
        description:
          "Node.js is my current main programming language since the last 2 Years",
        subskills: [
          "Express",
          "WS",
          "OAuth2",
          "Crypto",
          "IOTA.js Library"
        ]
      },
      {
        skill: "Vue.js",
        skilllevel: 3,
        description:
          "Developed some pages with Vue",
        subskills: [
          "AMCharts",
          "D3",
          "charts.js",
          "Vuetify"
        ]
      },
      {
        skill: "Python",
        skilllevel: 3,
        description:
          "Many data science, machine learning and statistics experiences, but only university level experience",
        subskills: [
          "Mathplotlib",
          "Scikitlearn",
          "Tensorflow",
          "Numpy",
          "Pandas"
        ]
      },
      {
        skill: "C++/C",
        skilllevel: 2,
        description:
          "Some experiences in personal and university projects such as an low-level Operating System, and a drone flight controller",
        subskills: [
          "PID Controller",
          "OS Scheduling",
          "Read and Write to GPIO",
          "SPI",
          "I2C"
        ]
      },
      {
        skill: "Databases",
        skilllevel: 4,
        description:
          "Developed database systems with all major paradigms",
        subskills: [
          "MongoDB",
          "MySQL/MariaDB",
          "DynamoDB",
          "Redis"
        ]
      }
    ]
  })
};
</script>
