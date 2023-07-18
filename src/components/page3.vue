<template>
  <div style="background: #c0392b">
    <svg width="100%" viewBox="0 0 1000 31" version="1.1" class="wave-svg">
      <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
        <path d="M1021,31.3211002 L1021,11.1726624 C1021,11.1726624 912.046875,24.8132884 717.960938,24.8132884 C523.875,24.8132884 398.609375,-0.534368356 243.921875,0.00860021491 C89.234375,0.551568786 -3,9.73858068 -3,9.73858068 L-3,31.3211002 L1021,31.3211002 Z" id="Fill-8" fill="#222222"></path>
      </g>
    </svg>
  </div>
  <div id="schedule">
    <div class="min-h-screen text-white p-10">
      <div class="lg:mt-14">
        <div class="text-center">
          <h1 class="text-4xl md:text-6xl">日程安排</h1>
          <p class="mt-5 font-serif">日程安排将随时更新</p>
        </div>
        <div class="flex justify-center">
          <div class="py-36 md:w-1/3">
            <ol class="schedule-list">
              <li v-for="item in timetable" :class="item.special">
                <time>{{ item.time }}</time>
                <h4 v-if="item.speaker">演讲者：{{ item.speaker }}</h4>
                <h3>{{ item.theme }}</h3>
                <div v-if="item.information" class="introduce">
                  <p>{{ item.information }}</p>
                </div>
              </li>
            </ol>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'page3',
  data() {
    return {
      timetable: [
        {
          special: 'start',
          time: '9:30',
          speaker: '即将揭晓',
          theme: '即将揭晓',
          information: '即将揭晓'
        },
        {
          time: '10:30',
          speaker: '即将揭晓',
          theme: '即将揭晓',
          information: '即将揭晓'
        },
        {
          time: '11:05',
          speaker: '即将揭晓',
          theme: '即将揭晓',
          information: '即将揭晓'
        },
        {
          time: '11:40',
          speaker: '即将揭晓',
          theme: '即将揭晓',
          information: '即将揭晓'
        },
        {
          special: 'walk',
          time: '12:15',
          theme: '中午休息、午餐'
        },
        {
          time: '13:40',
          speaker: '即将揭晓',
          theme: '即将揭晓',
          information: '即将揭晓'
        },
        {
          time: '14:15',
          speaker: '即将揭晓',
          theme: '即将揭晓',
          information: '即将揭晓'
        },
        {
          time: '14:50',
          speaker: '即将揭晓',
          theme: '即将揭晓',
          information: '即将揭晓'
        },
        {
          special: 'walk',
          time: '15:25',
          theme: '茶歇'
        },
        {
          time: '16:20',
          speaker: '即将揭晓',
          theme: '即将揭晓',
          information: '即将揭晓'
        },
        {
          time: '16:55',
          speaker: '即将揭晓',
          theme: '即将揭晓',
          information: '即将揭晓'
        },
        {
          time: '17:35',
          speaker: '尤雨溪',
          theme: '主题演讲',
          information: '即将揭晓'
        },
        {
          special: 'end',
          time: '18:30',
          theme: '结束'
        }
      ]
    }
  },
  components: {
  }
}
</script>

<style scoped>
#schedule {
  background: #222222;
}
.schedule-list {
  padding-left: 90px
}

.sponsors-list td {
  padding-bottom: 60px;
  text-align: center
}

.schedule-list > li {
  border-left: 8px solid #f7df1e;
  padding: 0 0 40px 20px;
  position: relative;
}

.schedule-list li time {
  color: #999;
  font-size: 14px;
  left: -125px;
  position: absolute;
  text-align: right;
  top: 16px;
  width: 100px
}

.schedule-list li h3 {
  color: #ddd;
  font-size: 16px;
  margin-bottom: 10px;
  text-align: left
}

.schedule-list li h4,.introduce {
  color: #999;
  font-size: 14px
}

.schedule-list li h3 a {
  margin-right: 1rem
}

.schedule-list li h3 img {
  vertical-align: middle
}

.schedule-list li.walk {
  border-left: 8px dotted #666
}

.schedule-list li.end {
  padding-bottom: 1px
}

.schedule-list li:before {
  background-color: #f7df1e;
  content: "";
  display: block;
  height: 8px;
  left: 0;
  position: absolute;
  top: 24px;
  width: 8px
}

.schedule-list li.walk::before {
  background-color: transparent
}

.schedule-list li.start time {
  top: -6px;
}

.schedule-list li.end time,.schedule-list li.walk time {
  top: 22px
}

.schedule-list li.start:before,.schedule-list li.end:before {
  background-color: #222;
  border: 3px solid #fff;
  border-radius: 50%;
  content: "";
  display: block;
  height: 12px;
  left: -13px;
  position: absolute;
  width: 12px
}

.schedule-list li.start:before {
  background-color: #fff;
  top: -4px
}

.schedule-list li.end:before {
  bottom: 0
}

</style>
