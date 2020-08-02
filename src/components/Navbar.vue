<template>
    <nav>
        <v-app-bar flat app>
                <v-app-bar-nav-icon class="grey--text" @click="drawer=!drawer"></v-app-bar-nav-icon>            <v-toolbar-title class="text-uppercase grey--text">
                <span class="font-weight-light">Salvan</span>
                <span>Todo</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn text color="grey">
                <span>Sign Out</span>
                <v-icon right>exit_to_app</v-icon>
            </v-btn>
        </v-app-bar>

        <v-navigation-drawer v-model="drawer" class="indigo" app>
            <p >test</p>
        </v-navigation-drawer>
    </nav>
</template>

<script>
export default {
    data(){
        return{
            drawer:false,
        }
    }
};
</script>