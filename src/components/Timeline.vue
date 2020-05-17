<template>
  <v-container>
    <v-timeline align-top :dense="$vuetify.breakpoint.smAndDown">
      <v-timeline-item
        color="primary"
        :icon="item.icon"
        fill-dot
        v-for="(item, i) in items"
        :key="i"
      >
        <template v-slot:opposite>
          <span class="headline font-weight-bold">{{ item.year }}</span>
        </template>
        <v-card color="primary" dark>
          <div class="title-box">
            <div class="title-text-box">
              <v-card-title class="title">{{ item.title }}</v-card-title>
              <v-card-subtitle>{{ item.subtitle }}</v-card-subtitle>
            </div>
          </div>
          <v-card-text class="white text--primary">
            <div class="card-text-img">{{ item.description }}</div>
            <v-img :src="item.image" max-height="200" contain></v-img>
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script>
export default {
  name: "Timeline",

  data: () => ({
    items: [
      {
        title: "Student Assistant at Werzeugmaschinenlabor RWTH Aachen",
        subtitle: "Product Management - Backend Development",
        year: "2018",
        icon: "fa-user",
        description:
          "Development of a cloud based big data processing tool with build in dlt support.",
        image: "/assets/wzl-desc.jpg"
      },
      {
        title: "B. Sc. Computer Science",
        subtitle: "Model-based development of distributed trajectory planning system for autonomous vehicles",
        year: "2019",
        icon: "fa-graduation-cap",
        description:
          "The thesis was about developing an autonomously driving car with an model-based approach build on the robot operating system and embedded monti arc math. A hybrid system of aPID controller and a trajectory planner is used to control the car. Thus an autonomously driving car is simulated as close to reality as possible. The driving properties are taken over by the physics engine of TORCS, an open racing car simulator. The model-based approach should utilize potential synergies between software development and mechanichal / electrical engineering.",
        image: "/assets/rwth-desc.png"
      },
      {
        title: "Fullstack Developer at Senseering GmbH",
        subtitle: "Backend Development - Distibuted Ledger Solutions",
        year: "2020",
        icon: "fa-briefcase",
        description:
          "Knowledge in all important areas of AWS, for example in EC2, Route 53 and S3",
        image: "/assets/senseering-desc.png"
      }
    ],
  })
};
</script>
