<template>
    <v-navigation-drawer expand-on-hover rail class="bg-blue-grey-darken-3">
        <v-list>
            <v-list-item prepend-avatar="https://cdn-icons-png.flaticon.com/512/508/508970.png" class="text-center"
                title="SISCE" subtitle="ALUMNO"></v-list-item>
            <v-divider></v-divider>
            <v-list-item prepend-avatar="https://cdn-icons-png.freepik.com/512/194/194935.png"
                title="Rawy De Los Santos Fernandez" subtitle="202T0480">
            </v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list :lines="false" density="compact" nav permanent>
            <v-list-item title="Opciones" value="opciones"></v-list-item>
            <v-list-item v-for="(item, i) in items" :key="i" :value="items" color="black">
                <template v-slot:prepend>
                    <v-icon :icon="item.icon"></v-icon>
                </template>

                <v-list-item-title v-text="item.text"></v-list-item-title>
            </v-list-item>
        </v-list>


        <template v-slot:append>
            <div>
                <v-list-item prepend-icon="mdi-exit-to-app" class="bg-red-darken-4">
                    Salir
                </v-list-item>
            </div>
        </template>

    </v-navigation-drawer>
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