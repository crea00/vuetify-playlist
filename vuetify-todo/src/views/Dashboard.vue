<template>
  <div class="dashboard">
    <h1 class="subheading grey--text">Dashboard</h1>

      <v-container class="my-5">

        <v-card flat v-for="project in projects" :key="project.title">
          <v-layout row wrap :class="`pa-3 project ${project.status}`">
            <v-flex xs12 md6>
              <div class="caption grey--text">Project Title</div>
              <div>{{ project.title }}</div>
            </v-flex>
            <v-flex xs6 sm4 md2>
              <div class="caption grey--text">Person</div>
              <div>{{ project.person }}</div>
            </v-flex>
            <v-flex xs6 sm4 md2>
              <div class="caption grey--text">Due by</div>
              <div>{{ project.due }}</div>
            </v-flex>
            <v-flex xs6 sm4 md2>
              <div class="caption grey--text">Status</div>
              <div>{{ project.status }}</div>
            </v-flex>
          </v-layout>
          <v-divider></v-divider>
        </v-card>

    </v-container>

  </div>
</template>

<script>
export default {
  name: 'Dashboard',
  data() {
    return {
      projects: [
        { title: 'Design a new website', person: 'Jerome', due: '1st Jan 2019', status: 'ongoing', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. In expedita adipisci iste commodi nesciunt. Cupiditate nemo, minima earum at ab rerum, iure nostrum omnis consequuntur eos tempora, perspiciatis autem aut!' },
        { title: 'Code up the homepage', person: 'Chun Li', due: '10th Jan 2019', status: 'complete', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. In expedita adipisci iste commodi nesciunt. Cupiditate nemo, minima earum at ab rerum, iure nostrum omnis consequuntur eos tempora, perspiciatis autem aut!' },
        { title: 'Design video thumbnails', person: 'Ryu', due: '20th Dec 2018', status: 'complete', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. In expedita adipisci iste commodi nesciunt. Cupiditate nemo, minima earum at ab rerum, iure nostrum omnis consequuntur eos tempora, perspiciatis autem aut!' },
        { title: 'Create a community forum', person: 'Gouken', due: '20th Oct 2018', status: 'overdue', content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. In expedita adipisci iste commodi nesciunt. Cupiditate nemo, minima earum at ab rerum, iure nostrum omnis consequuntur eos tempora, perspiciatis autem aut!' },
      ]
    }
  }

}
</script>

<style>
.project.complete {
  border-left: 4px solid #3cd1c2;
}
.project.ongoing {
  border-left: 4px solid orange;
}
.project.overdue {
  border-left: 4px solid tomato;
}
</style>

