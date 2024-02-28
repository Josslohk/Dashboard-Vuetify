<template>
    <v-card color="grey-darken-4">
        <div class="mt-2 text-uppercase text-center">
            <h2 class="font-weight-medium text-grey-lighten-5">SICE
                <span class="text-grey">ALUMNOS</span>
            </h2>
        </div>
        <v-list>
            <v-list-item prepend-avatar="https://cdn.vuetifyjs.com/images/john.png" title="John Leider"
                subtitle="john@google.com">
            </v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list :lines="false" density="compact" nav permanent>
            <v-list-item v-for="(item, i) in items" :key="i" :value="items" color="black">
                <template v-slot:prepend>
                    <v-icon :icon="item.icon"></v-icon>
                </template>

                <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item>
        </v-list>
<!-- 
        <template v-slot:append>
            <div class="pa-2">
                <v-btn block class="bg-grey">
                    Logout
                </v-btn>
            </div>
        </template> -->

        <template v-slot:append>
            <div>
                <v-list-item prepend-icon="mdi-exit-to-app" class="bg-red-darken-4">
                    Salir
                </v-list-item>
            </div>
        </template>

    </v-card>
    <!-- <v-main style="height: 100vh"></v-main> -->
</template> 

<script>
export default {
    data: () => ({
        items: [
            { text: 'Datos Generales', icon: 'mdi-folder' },
            { text: 'Horarios', icon: 'mdi-calendar-account-outline' },
            { text: 'Calificaciones', icon: 'mdi-book-education' },
            { text: 'Kardex', icon: 'mdi-school' },
            { text: 'Reinscripcion', icon: 'mdi-account-group' },
            { text: 'Pago de servicios', icon: 'mdi-account-cash' },
            { text: 'Encuesta de carga', icon: 'mdi-poll' },
        ],
    }),
}
</script>
