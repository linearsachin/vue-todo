<template>
  <div class="home">
    <h1>Homepage</h1>

    <v-btn class="pink white--text">Click</v-btn>
    <br><br>
    <v-btn depressed color="pink">click</v-btn><br><br>
    <v-btn text color="pink">click</v-btn><br><br>

    <v-btn depressed class="pink white--textss">
      <v-icon left>email</v-icon>
      <span>Email </span>
    </v-btn><br><br>

    <v-btn depressed small class="pink white--textss">
      <v-icon left small>email</v-icon>
      <span>Email </span>
    </v-btn><br><br>

    <v-btn depressed large class="pink white--textss">
      <span left>Email</span>
      <v-icon large right>email</v-icon>
    </v-btn><br><br>

    <v-btn fab depressed small dark class="purple white--textss">
      <v-icon>favorite</v-icon>
    </v-btn><br><br>


  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: 'Home',
  components: {
  }
}
</script>
