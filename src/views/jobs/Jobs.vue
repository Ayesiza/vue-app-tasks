<template>
    
    <div  >
        <h1>Jobs Available</h1>
         <button @click="toggleJobs">open Jobs</button>
        <div v-if="showJobs">
        <div v-for="job in jobs" :key="job.id"  >
            <router-link :to="{ name:'JobDetails', params: {id: job.id}}">
 <h2>{{job.title}}</h2>
            </router-link>
           
        </div>
       
        </div>
       

    </div>
</template>

<script>
export default {
    data() {
        return{
            jobs:[
                {title:"Web Developer", id:1, detaile:'lorem'},
                {title:"Web Designer", id:2, detaile:'lorem'},
                {title:"Software Engineer", id:3, detaile:'lorem'},
            ],
            showJobs:false,
        }

    },
    methods:{
        toggleJobs() {
            this.showJobs=!this.showJobs
        }
    }
    
}
</script>

<style scoped>

</style>