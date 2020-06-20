<template>
    <div class="container">
        <ListDefault :elements-list="elements"/>
    </div>
</template>

<script>

import ListDefault from '../partials/_ListDefault'

export default {

    components: {
        ListDefault
    },
    created(){
        this.findAll()
    },
    data(){
        return{
            elements: []
        };
    },
    methods: {
        findAll: function(){
            fetch('http://localhost:8000/api/category/'+this.$route.params.id+'/elemets/?format=json') 
                .then(res => res.json())
                .then(res => this.elements = res)                
        }
    },
}
</script>

<style>
    .box{
        border: 3px solid #CCC;
        margin: 5px 0 0 0;
    }
    
</style>