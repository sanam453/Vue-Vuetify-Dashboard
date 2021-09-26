<template>
  <div class="dashboard">
    <h1  class="subheading grey--text">Team</h1>

    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
          <v-card class="text-center ma-5">
            <v-responsive class="pt-4">
              <v-avatar size="100" class="grey lighten-2">
                <img :src="person.avatar" alt="">
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{person.name}}</div>
              <div class="grey--text">{{person.role}}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn text color="grey">
                <v-icon small left>message</v-icon>
                <span>message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>

    </v-container>
</div>
</template>

<script>

export default {
  data() {
    return {
      team: [
        { name: 'Lina', role: 'Web Designer', avatar: '/avatar-4.jpeg' },
        { name: 'Dina', role: 'Web Developer', avatar: '/avatar-2.jpg' },
        { name: 'Heena', role: 'Software Engineer', avatar: '/avatar-3.jpg' },
        { name: 'Meena', role: 'Digital Creator', avatar: '/avatar-1.jpg' },
      ]
    }
  }
 
  }
</script>
