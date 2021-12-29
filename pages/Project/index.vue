<template>
  <div>
    <Header />
    <h3>Project Page</h3>
    <div>
      <div v-for="project in projects" :key="project.id">
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
export default {
  name: "Project",
  data() {
    return {
      projects: [
        {
          id: 1,
          name: "project 1",
          detail: "ini project 1",
        },
        {
          id: 2,
          name: "project 2",
          detail: "ini project 2",
        },
        {
          id: 3,
          name: "project 3",
          detail: "ini project 3",
        },
      ],
    };
  },
};
</script>

<style></style>
