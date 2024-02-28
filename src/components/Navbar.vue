<template>
    <nav>
        <v-toolbar v-app>
            <v-app-bar-nav-icon class="text-grey" @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-toolbar-tittle class="text-uppercase text-grey">
                <span class="font-weight-light">SI</span>
                <span>CE</span>
            </v-toolbar-tittle>
            <v-spacer></v-spacer>
            <v-btn variant="plain" class="text-grey">
                <span>Sing Out</span>
                <v-icon class="right" icon="mdi-exit-to-app"></v-icon>
            </v-btn>
        </v-toolbar>
        <!-- <Dashboard></Dashboard>-->
        <v-navigation-drawer v-app v-model="drawer" class="bg-transparent ">
        </v-navigation-drawer>
    </nav>
</template>

<script>
// import Dashboard from './DashboardComponent.vue';

export default {
    // components: { Dashboard },
    data() {
        return {
            drawer: false
        }
    }
}
</script>