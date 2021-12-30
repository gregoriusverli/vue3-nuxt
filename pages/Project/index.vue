<template>
  <div>
    <Header />
    <h3>Project Page {{ state.name }}</h3>
    <div>
      <div v-for="project in state.projects" :key="project.id">
        <div class="p-1">
          <nuxt-link
            class="block text-black hover:text-red-500"
            :to="`/project/${project.id}`"
          >
            {{ project.name }}
          </nuxt-link>

          <p>{{ project.detail }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { onMounted, reactive } from "@nuxtjs/composition-api";
import axios from "axios";
export default {
  name: "Project",
  setup() {
    const state = reactive({
      name: "verliyaaaaaaa",
      projects: [],
    });

    onMounted(async () => {
      await axios("https://jsonplaceholder.typicode.com/users")
        .then((response) => {
          console.log(response.data, "ress");
          state.projects = response.data;
        })
        .catch((err) => {
          console.log(err, "error");
        });
    });

    return { state };
  },
};
</script>

<style></style>
