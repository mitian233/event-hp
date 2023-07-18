<template>
  <div id="sponsors">
    <div class="min-h-screen p-10">
      <div class="text-center">
        <h1 class="lg:mt-10 text-4xl md:text-6xl">宣传合作</h1>
      </div>
      <div class="flex justify-center">
        <ul class="lg:flex lg:max-w-5xl flex-row flex-wrap text-center justify-between">
          <li v-for="item in sponsors" class="p-5">
            <a :href="item.site"><img class="w-48 inline-block" :src="item.image" :alt="item.name"/></a>
            <p>{{ item.name }}</p>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: 'page5',
  data: () => {
    return {
      sponsors:[
        {
          image: 'https://img.w3ctech.com/bowen.png',
          name: '合作方',
          site: 'http://www.broadview.com.cn/'
        },
        {
          image: 'https://img.w3ctech.com/turing-logo.png',
          name: '合作方',
          site: 'http://www.ituring.com.cn/'
        },
        {
          image: 'https://img.w3ctech.com/juejin-logo.png',
          name: '支持社区',
          site: 'http://gold.xitu.io/'
        },
        {
          image: 'https://img.w3ctech.com/w3c-plus-400.png',
          name: '支持社区',
          site: 'http://www.w3cplus.com/'
        },
        {
          image: 'https://img.w3ctech.com/zdk_400.png',
          name: '支持社区',
          site: 'https://zdk.f2er.net/'
        },
      ]
    }
  }
}
</script>

<style scoped>
#sponsors {
  background-color: #f5f5f5;
}
</style>
