<template>
  <div id="app">
    <input value="刷新" @click="getSchedulerList" type="button">
<!--    <SchedulerList />-->
    <PodList v-bind:SchedulerList="SchedulerList" ></PodList>
<!--    <SchedulerItem v-if="SchedulerList.length > index" v-bind:SchedulerItem="SchedulerList[index]"></SchedulerItem>-->
  </div>

</template>

<script>

// import SchedulerList from "@/components/SchedulerList";
// import SchedulerItem from "@/components/SchedulerItem";
import VueResource from 'vue-resource'
import Vue from "vue";
import PodList from "@/components/PodList";

Vue.use(VueResource)


export default {
  name: 'App',
  components: {
    PodList,
  },
  data () {
    return {
      SchedulerList: [],
      index: 1
    }
  },
  methods: {
    getSchedulerList () {
    this.$http.get('http://192.168.1.201:8080/getSchedulerList').then(response => {
        console.log(response);
        this.SchedulerList=response.body
        console.log(this.SchedulerList)
      })
    }

  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
