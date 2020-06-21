<template>
    <div>        
        <b-card>
            <h1>{{ element.title }}</h1>
            <div class="p-3">
                <b-card-text>{{ element.description }}</b-card-text>
            </div>             
        </b-card>      
    </div>
</template>

<script>
export default {
    created(){
        this.find();
    },
    data(){
        return{
            element: Object
        };
    },
    methods: {
        find: function(){
            fetch("http://127.0.0.1:8000/api/element/"+this.$route.params.id+"/?format=json") 
                .then(res => res.json())
                .then(res => this.element = res)                
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