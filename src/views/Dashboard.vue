<template>
  <div class="dashboard">
    <h1 class="subheading grey--text">Homepage</h1>
    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 md6>
          <v-btn  block class="primary" outlined>1</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outlined block class="primary">2</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outlined block class="primary">3</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outlined block class="primary">4</v-btn>
        </v-flex>
      </v-layout>

      <v-layout row wrap justify-space-around="">
        <v-flex xs4 md3>
          <v-btn outlined block color="success">1</v-btn>
        </v-flex>
        <v-flex xs4 md3>
          <v-btn outlined block color="success">2</v-btn>
        </v-flex>
        <v-flex xs4 md3>
          <v-btn outlined block color="success">3</v-btn>
        </v-flex>

      </v-layout>
    </v-container>


  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'dashboard',
  components: {
  }
}
</script>
