<template>
  <table class="table table-striped table-bordered table-hover">
    <caption>caption</caption>
    <thead>
    <tr >
      <th >#</th>
      <th>内存</th>
      <th>磁盘</th>
      <th>CPU</th>
      <th>时延</th>
      <th>优选分数</th>
      <th>Spread分数</th>
    </tr>
    </thead>
    <tbody>
    <tr v-for="item in SchedulerItem.NodeArr" :key="item.id">
      <td>{{item}}</td>
      <td>{{Fix2(SchedulerItem.ScoreMap[item].MemScore)}}</td>
      <td>{{Fix2(SchedulerItem.ScoreMap[item].DiskScore)}}</td>
      <td>{{Fix2(SchedulerItem.ScoreMap[item].CpuScore)}}</td>
      <td>{{Fix2(SchedulerItem.ScoreMap[item].DelayScore)}}</td>
      <td>{{Fix2(SchedulerItem.PrioritizeScoreMap[item])}}</td>
      <td>{{Fix2(SchedulerItem.SpreadScore[item])}}</td>
    </tr>
    </tbody>
  </table>
</template>

<script>

export default {
  name: "SchedulerItem",
  props: ['SchedulerItem'],
  methods: {
    Fix2(val){
      return Number(val).toFixed(2);
    },
  }
}
</script>

<style scoped>

</style>