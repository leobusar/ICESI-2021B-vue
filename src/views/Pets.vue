<template>
    <v-container grid-list-md fluid>
        <v-layout wrap>
            <v-flex xs12 sm4 md3 v-for="dog in dogs" :key="dog.breed">
                <v-card color="grey lighten-2">
                    <v-img :src="dog.img" height="170px"></v-img>
                    <v-card-title>
                        <div>
                            <h4>
                                {{ dog.name }}
                            </h4>
                            <p>{{dog.breed}}</p>
                        </div>
                    </v-card-title>
                </v-card>
            </v-flex>
        </v-layout>
    </v-container>
</template>
<script>
import  {Dogs} from '../data/dogs'

export default {
    data: () => {
        return {
            dogs: Dogs
        }
    }
    
}
</script>