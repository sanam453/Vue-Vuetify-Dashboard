<template>
  <div class="projects">
    <h1 class="subheading grey--text">Projects</h1>


    <v-container class="my-5">
      <v-expansion-panels>
          <v-expansion-panel v-for="project in myProjects" :key="project.title">
            <v-expansion-panel-header class="py-1">
              {{ project.title }}
            </v-expansion-panel-header>
            <v-expansion-panel-content>
              <div class="px-4 grey--text">
                <div class="font-weight-bold">Due by {{ project.due }}</div>
                <div>{{ project.content }}</div>
              </div>
            </v-expansion-panel-content>
        </v-expansion-panel>
      </v-expansion-panels>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: "Design a new website",
          person: "The Lady Dina",
          due: "1st Jan 2019",
          status: "ongoing",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt consequuntur eos eligendi illum minima adipisci deleniti, dicta mollitia enim explicabo fugiat quidem ducimus praesentium voluptates porro molestias non sequi animi!"
        },
        {
          title: "Code up the homepage",
          person: "Meena",
          due: "10th Jan 2019",
          status: "complete",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt consequuntur eos eligendi illum minima adipisci deleniti, dicta mollitia enim explicabo fugiat quidem ducimus praesentium voluptates porro molestias non sequi animi!"
        },
        {
          title: "Design video thumbnails",
          person: "Heena",
          due: "20th Dec 2018",
          status: "complete",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt consequuntur eos eligendi illum minima adipisci deleniti, dicta mollitia enim explicabo fugiat quidem ducimus praesentium voluptates porro molestias non sequi animi!"
        },
        {
          title: "Create a community forum",
          person: "Lina",
          due: "20th Oct 2018",
          status: "overdue",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Sunt consequuntur eos eligendi illum minima adipisci deleniti, dicta mollitia enim explicabo fugiat quidem ducimus praesentium voluptates porro molestias non sequi animi!"
        }
      ]
    };
  },
  computed: {
    myProjects() {
      return this.projects.filter(
        (project) => 
        
    project.person === 'The Lady Dina' && project.status !== 'complete'   ,
      );       
 
    }
  }
};
</script>