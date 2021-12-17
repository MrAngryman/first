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
  name: "SchedulerList",
  // props: ['SchedulerItem'],
  data () {
    return {
      SchedulerList: [{
        "ScoreMap": {
          "pitboss1": {
            "CpuScore": 29.64592571892873,
            "MemScore": 10.956037215398124,
            "DiskScore": 10,
            "DelayScore": 16
          },
          "pitboss2": {
            "CpuScore": 29.77632565408559,
            "MemScore": 8.094705179105464,
            "DiskScore": 3.9090775967209543,
            "DelayScore": 16
          },
          "pitboss3": {
            "CpuScore": 29.440046564324827,
            "MemScore": 9.02994989562382,
            "DiskScore": 8.441363573531131,
            "DelayScore": 16
          },
          "pitboss4": {
            "CpuScore": 29.999999999999996,
            "MemScore": 3.328394307345604,
            "DiskScore": 1.191798873748592,
            "DelayScore": 16
          },
          "pitboss5": {
            "CpuScore": 29.18880286877221,
            "MemScore": 20,
            "DiskScore": 8.167741078127541,
            "DelayScore": 16
          }
        },
        "PodName": "nginx-7848d4b86f-q477r",
        "PrioritizeScoreMap": {
          "pitboss1": 66.60196293432685,
          "pitboss2": 57.78010842991201,
          "pitboss3": 62.91136003347978,
          "pitboss4": 50.520193181094186,
          "pitboss5": 73.35654394689976
        },
        "SpreadScore": {
          "pitboss1": 100,
          "pitboss2": 100,
          "pitboss3": 100,
          "pitboss4": 100,
          "pitboss5": 100
        },
        "NodeArr": ["pitboss4", "pitboss5", "pitboss1", "pitboss2", "pitboss3"]
      },
        {
        "ScoreMap": {
          "pitboss1": {
            "CpuScore": 29.283849767926636,
            "MemScore": 5.051293413742176,
            "DiskScore": 2.3558132617357126,
            "DelayScore": 16
          },
          "pitboss2": {
            "CpuScore": 29.7661514144205,
            "MemScore": 13.189649499828874,
            "DiskScore": 10,
            "DelayScore": 16
          },
          "pitboss3": {
            "CpuScore": 29.868847938945358,
            "MemScore": 6.866301700327838,
            "DiskScore": 8.72557109411401,
            "DelayScore": 16
          },
          "pitboss4": {
            "CpuScore": 29.602432699960314,
            "MemScore": 6.54160867011941,
            "DiskScore": 3.3983161410170593,
            "DelayScore": 16
          },
          "pitboss5": {
            "CpuScore": 30,
            "MemScore": 20,
            "DiskScore": 8.07798356593809,
            "DelayScore": 16
          }
        },
        "PodName": "nginx-7848d4b86f-ntgdd",
        "PrioritizeScoreMap": {
          "pitboss1": 52.690956443404524,
          "pitboss2": 68.95580091424938,
          "pitboss3": 61.460720733387205,
          "pitboss4": 55.54235751109679,
          "pitboss5": 74.0779835659381
        },
        "SpreadScore": {
          "pitboss1": 100,
          "pitboss2": 100,
          "pitboss3": 100,
          "pitboss4": 100,
          "pitboss5": 0
        },
        "NodeArr": ["pitboss1", "pitboss2", "pitboss3", "pitboss4", "pitboss5"]
      },
        {
        "ScoreMap": {
          "pitboss1": {
            "CpuScore": 29.55333717638107,
            "MemScore": 1.2124308514017028,
            "DiskScore": 10,
            "DelayScore": 16
          },
          "pitboss2": {
            "CpuScore": 30,
            "MemScore": 3.553298686845226,
            "DiskScore": 7.819084247835172,
            "DelayScore": 16
          },
          "pitboss3": {
            "CpuScore": 29.630479724805365,
            "MemScore": 5.7115614516431865,
            "DiskScore": 6.1146989471908855,
            "DelayScore": 16
          },
          "pitboss4": {
            "CpuScore": 29.661449530168863,
            "MemScore": 0.5804322288656599,
            "DiskScore": 2.2878996012368438,
            "DelayScore": 16
          },
          "pitboss5": {
            "CpuScore": 29.534384175607062,
            "MemScore": 20,
            "DiskScore": 1.1481329540294212,
            "DelayScore": 16
          }
        },
        "PodName": "nginx-7848d4b86f-hp469",
        "PrioritizeScoreMap": {
          "pitboss1": 56.76576802778277,
          "pitboss2": 57.372382934680395,
          "pitboss3": 57.45674012363944,
          "pitboss4": 48.529781360271365,
          "pitboss5": 66.68251712963648
        },
        "SpreadScore": {
          "pitboss1": 100,
          "pitboss2": 0,
          "pitboss3": 100,
          "pitboss4": 100,
          "pitboss5": 0
        },
        "NodeArr": ["pitboss5", "pitboss1", "pitboss2", "pitboss3", "pitboss4"]
      },
        {
        "ScoreMap": {
          "pitboss1": {
            "CpuScore": 30,
            "MemScore": 20,
            "DiskScore": 1.1067557724565098,
            "DelayScore": 16
          },
          "pitboss2": {
            "CpuScore": 28.964916284953823,
            "MemScore": 1.6613188269014938,
            "DiskScore": 2.524458044878916,
            "DelayScore": 16
          },
          "pitboss3": {
            "CpuScore": 29.41536582327611,
            "MemScore": 5.400836834285344,
            "DiskScore": 3.5378442720736203,
            "DelayScore": 16
          },
          "pitboss4": {
            "CpuScore": 29.644508777901837,
            "MemScore": 5.6697529019912025,
            "DiskScore": 3.203488706909104,
            "DelayScore": 16
          },
          "pitboss5": {
            "CpuScore": 29.25164372723234,
            "MemScore": 8.09080864296766,
            "DiskScore": 10,
            "DelayScore": 16
          }
        },
        "PodName": "nginx-7848d4b86f-nt9pf",
        "PrioritizeScoreMap": {
          "pitboss1": 67.10675577245651,
          "pitboss2": 49.150693156734235,
          "pitboss3": 54.354046929635075,
          "pitboss4": 54.51775038680214,
          "pitboss5": 63.3424523702
        },
        "SpreadScore": {
          "pitboss1": 100,
          "pitboss2": 0,
          "pitboss3": 0,
          "pitboss4": 100,
          "pitboss5": 0
        },
        "NodeArr": ["pitboss4", "pitboss5", "pitboss1", "pitboss2", "pitboss3"]
      },
        {
        "ScoreMap": {
          "pitboss1": {
            "CpuScore": 29.740380150279584,
            "MemScore": 14.297224932877896,
            "DiskScore": 10,
            "DelayScore": 16
          },
          "pitboss2": {
            "CpuScore": 29.70111610619394,
            "MemScore": 1.9024600047148565,
            "DiskScore": 5.037564711851656,
            "DelayScore": 16
          },
          "pitboss3": {
            "CpuScore": 29.69368289082284,
            "MemScore": 20,
            "DiskScore": 3.5544338480200457,
            "DelayScore": 16
          },
          "pitboss4": {
            "CpuScore": 29.684560376034273,
            "MemScore": 15.536991509547315,
            "DiskScore": 8.182970896615513,
            "DelayScore": 16
          },
          "pitboss5": {
            "CpuScore": 30,
            "MemScore": 3.831107175590506,
            "DiskScore": 4.375771135747202,
            "DelayScore": 16
          }
        },
        "PodName": "nginx-7848d4b86f-mvbzx",
        "PrioritizeScoreMap": {
          "pitboss1": 70.03760508315747,
          "pitboss2": 52.641140822760455,
          "pitboss3": 69.2481167388429,
          "pitboss4": 69.4045227821971,
          "pitboss5": 54.206878311337704
        },
        "SpreadScore": {
          "pitboss1": 0,
          "pitboss2": 0,
          "pitboss3": 0,
          "pitboss4": 100,
          "pitboss5": 0
        },
        "NodeArr": ["pitboss5", "pitboss1", "pitboss2", "pitboss3", "pitboss4"]
      }],
      SchedulerItem: {
        "ScoreMap": {
          "pitboss1": {
            "CpuScore": 29.64592571892873,
            "MemScore": 10.956037215398124,
            "DiskScore": 10,
            "DelayScore": 16
          },
          "pitboss2": {
            "CpuScore": 29.77632565408559,
            "MemScore": 8.094705179105464,
            "DiskScore": 3.9090775967209543,
            "DelayScore": 16
          },
          "pitboss3": {
            "CpuScore": 29.440046564324827,
            "MemScore": 9.02994989562382,
            "DiskScore": 8.441363573531131,
            "DelayScore": 16
          },
          "pitboss4": {
            "CpuScore": 29.999999999999996,
            "MemScore": 3.328394307345604,
            "DiskScore": 1.191798873748592,
            "DelayScore": 16
          },
          "pitboss5": {
            "CpuScore": 29.18880286877221,
            "MemScore": 20,
            "DiskScore": 8.167741078127541,
            "DelayScore": 16
          }
        },
        "PodName": "nginx-7848d4b86f-q477r",
        "PrioritizeScoreMap": {
          "pitboss1": 66.60196293432685,
          "pitboss2": 57.78010842991201,
          "pitboss3": 62.91136003347978,
          "pitboss4": 50.520193181094186,
          "pitboss5": 73.35654394689976
        },
        "SpreadScore": {
          "pitboss1": 100,
          "pitboss2": 100,
          "pitboss3": 100,
          "pitboss4": 100,
          "pitboss5": 100
        },
        "NodeArr": ["pitboss4", "pitboss5", "pitboss1", "pitboss2", "pitboss3"]
      }
    }
  },
  methods: {
    // insert: function () {
    //   this.users.push(this.user)
    // },
    // remove: function (index) {
    //   this.users.splice(index, 1)
    // }
    Fix2(val){
      return Number(val).toFixed(2);
    },
  }
}
</script>

<style scoped>

</style>