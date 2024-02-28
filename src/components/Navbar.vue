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
        <div class="d-md-none d-lg-flex">
            <DashboardMovil></DashboardMovil>
        </div>
        <div class="d-lg-none d-xl-none">
            <v-navigation-drawer permanent v-app v-model="drawer">
                <Dashboard></Dashboard>
                <!-- <main style="height: 100vh"></main> -->
            </v-navigation-drawer>
        </div>
    </nav>
</template>

<script>
import DashboardMovil from '@/components/vista en movil/DashboardMovil.vue';
import Dashboard from './DashboardComponent.vue';

export default {
    components: { Dashboard,DashboardMovil },
    data() {
        return {
            drawer: false
        }
    }
}
</script>
<!-- Alonsho -->