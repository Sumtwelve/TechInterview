<template>
  <v-container>
    <v-row>
      <v-col cols="6">
        <h2>Welcome to the Tech Interview</h2>
        You're doing great so far. Keep it up.
        <v-img
          alt="Cat with hat"
          class="shrink mr-2"
          contain
          src="../assets/catmeme.jpg"
          transition="scale-transition"
          width="100%"
        />
      </v-col>
      <v-col cols="6">
        <v-row>
          Something seems to be wrong. There should be a nav up there ^^^
        </v-row>
        <v-row>
          Add a nav to the view /data.
        </v-row>
      </v-col>
    </v-row>
    <v-row class="mx-auto">
      <v-col cols="4">
        <h2>Ecosystem</h2>
        <v-list>
          <v-list-item
            v-for="link in ecosystem"
            :key="link.href"
          >
            <a :href="link.href">{{ link.text }}</a>
          </v-list-item>
        </v-list>
      </v-col>
      <v-col cols="4">
        <h2>Important Links</h2>
        <v-list>
          <v-list-item
            v-for="link in importantLinks"
            :key="link.href"
          >
            <a :href="link.href">{{ link.text }}</a>
          </v-list-item>
        </v-list>
      </v-col>
      <v-col cols="4">
        <h2>What's Next</h2>
        <v-list>
          <v-list-item
            v-for="link in whatsNext"
            :key="link.href"
          >
            <a :href="link.href">{{ link.text }}</a>
          </v-list-item>
        </v-list>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",

  data: () => ({
    ecosystem: [
      {
        text: "vuetify-loader",
        href: "https://github.com/vuetifyjs/vuetify-loader",
      },
      {
        text: "github",
        href: "https://github.com/vuetifyjs/vuetify",
      },
      {
        text: "awesome-vuetify",
        href: "https://github.com/vuetifyjs/awesome-vuetify",
      },
    ],
    importantLinks: [
      {
        text: "Documentation",
        href: "https://vuetifyjs.com",
      },
      {
        text: "Chat",
        href: "https://community.vuetifyjs.com",
      },
      {
        text: "Made with Vuetify",
        href: "https://madewithvuejs.com/vuetify",
      },
      {
        text: "Twitter",
        href: "https://twitter.com/vuetifyjs",
      },
      {
        text: "Articles",
        href: "https://medium.com/vuetify",
      },
    ],
    whatsNext: [
      {
        text: "Explore components",
        href: "https://vuetifyjs.com/components/api-explorer",
      },
      {
        text: "Select a layout",
        href: "https://vuetifyjs.com/getting-started/pre-made-layouts",
      },
      {
        text: "Frequently Asked Questions",
        href: "https://vuetifyjs.com/getting-started/frequently-asked-questions",
      },
    ],
  }),
};
</script>
