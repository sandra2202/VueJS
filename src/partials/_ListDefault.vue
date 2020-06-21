<template>
    <div class="mt-3 mt-md-0">
        <div v-for="e in elementsList" v-bind:key="e.id">
            <router-link class="card-link" :to=" '/detail/' + e.id ">
                <b-card :header="e.title"
                header-bg-variant="primary"
                header-text-variant="white">
                    <b-card-text>{{ e.description }}</b-card-text> 
                </b-card>      
            </router-link>
        </div>
    </div>
</template>

<script>
export default {

    props:[
        'elementsList'
    ],
    data(){
        return{
            elements: []
        };
    },
    methods: {             
        
    },
}
</script>

<style>
    a.card-link,
    a.card-link:hover {
        color: #ff3399;
        text-decoration: none;
    }
    a.card-link:hover .card-body {
        background: #f8f9fa;
    }
    
</style>