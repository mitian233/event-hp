<template>
  <div class="text-white fixed top-1/3 right-10 bg-black bg-opacity-80 rounded z-50 hidden lg:block"
       style="writing-mode: vertical-rl;">
    <ul class="flex flex-row">
      <li>
        <a href="#about" @click.prevent="smoothScroll('#about')"><span data-letters="关于我们">关于</span></a>
      </li>
      <li>
        <a href="#speakers" @click.prevent="smoothScroll('#speakers')">嘉宾</a>
      </li>
      <li>
        <a href="#schedule" @click.prevent="smoothScroll('#schedule')">日程</a>
      </li>
      <li>
        <a href="#location" @click.prevent="smoothScroll('#location')">地点</a>
      </li>
      <li>
        <a href="#sponsors" @click.prevent="smoothScroll('#sponsors')">合作</a>
      </li>
      <li>
        <a href="https://vue.w3ctech.com/5">第五届</a>
      </li>
      <li>
        <a href="https://vue.w3ctech.com/1">第一届</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'sidebar',
  data() {
    return {};
  },
  methods: {
    smoothScroll: function(target) {
      const targetElement = document.querySelector(target);
      window.scrollTo({
        top: targetElement.offsetTop,
        behavior: 'smooth'
      });
    }
  }
};
</script>

<style>
li{
  font-family: "PingFang SC", "Helvetica Neue", Helvetica, "Microsoft Yahei", "HanHei SC", Arial, sans-serif;
  padding: 10px 2px 10px 2px;
}
</style>
