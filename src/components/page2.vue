<template>
  <div id="speakers" class="text-white">
    <div class="min-h-screen p-10">
      <div class="text-center">
        <h1 class=" md:text-6xl text-2xl lg:mt-10">演讲嘉宾</h1>
        <p class="mt-5 font-serif">与大牛一起探讨、持续更新中...</p>
      </div>
      <div class="flex flex-row flex-wrap justify-center mt-10 lg:justify-start">
        <ul v-for="card in experts" class="text-center m-10">
          <li>
            <a v-if="card.site === ''" href="/">
              <img :src="card.avatar" :alt="card.name" class="rounded-full avatar lg:w-64">
            </a>
            <a v-else :href="card.site">
              <img :src="card.avatar" :alt="card.name" class="rounded-full avatar lg:w-64">
            </a>
          </li>
          <li>
            <p class="font-bold">{{card.name}}</p>
            <p>{{card.introduction}}</p>
          </li>
        </ul>
      </div>
    </div>

  </div>
</template>

<script lang="ts">
export default {
  name: 'page2',
  data() {
    return {
      experts: [
        {
          name: '尤雨溪',
          introduction: '独立开源开发者 / Vue / Vite 作者',
          avatar: 'https://img.w3ctech.com/evan.jpg',
          site: ''
        },
      ]
    }
  },
  components: {
  }
}
</script>

<style scoped>
#speakers {
  background: #c0392b;
}
.avatar{
  border-top-left-radius: 59%;
  border-top-right-radius: 52%;
  border-bottom-left-radius: 59%;
  border-bottom-right-radius: 56%;
  -webkit-transform: rotate(-6deg);
  -ms-transform: rotate(-6deg);
  transform: rotate(-6deg);
  border: 3px solid #fff;
  -webkit-transition: all .3s ease-out;
  transition: all .3s ease-out;
}
.avatar:hover{
  border-radius: 50%;
  transform: rotate(0deg);
}
</style>
