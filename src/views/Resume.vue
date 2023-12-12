<script>
import ContentTable from '@/components/ContentTable.vue'
import Jobs from '@/models/jobs.json'
import Education from '@/models/education.json'
export default {
  name: "Resume",
  components: {ContentTable},
  data(){
    return{
      jobs: Jobs,
      education: Education,
    }
  },
  methods:{
    getHeader(item){
      let keys = Object.keys(item);
      let headers = [];
      keys.forEach((key) =>{
        headers.push(key.charAt(0).toUpperCase() + key.slice(1));
      });

      return headers;
    }
  }
}
</script>

<template>
  <div class="resume">
    <div class="work">
      <content-table
          :headers="getHeader(jobs[0])"
          :table-data="jobs"
          :title="'Work Experience'"/>
    </div>
    <div class="education">
      <content-table
          :headers="getHeader(education[0])"
          :table-data="education"
          :title="'Education'"/>
    </div>
  </div>
</template>

<style scoped>
.resume{
  display: flex;
  flex-flow: column nowrap;
}
.education{
  margin: 25px 0px 45px 0px;
}
</style>