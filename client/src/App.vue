<template>
  <div id="app">
    <img src="./assets/logo.png">
    <el-switch active-color="red" inactive-color="green" v-model="value1">
    </el-switch>
    <div class="block">
      <span class="demonstration">默认不区分颜色</span>
      <el-rate v-model="value2"></el-rate>
    </div>
    <div class="block">
      <span class="demonstration">区分颜色</span>
      <el-rate
        v-model="value3"
        :colors="['#99A9BF', '#F7BA2A', '#FF9900']">
      </el-rate>
    </div>
    <el-rate
      v-model="value4"
      :icon-classes="['icon-rate-face-1', 'icon-rate-face-2', 'icon-rate-face-3']"
      void-icon-class="icon-rate-face-off"
      :colors="['#99A9BF', '#F7BA2A', '#FF9900']">
    </el-rate>
    <el-rate
      v-model="value5"
      disabled
      show-score
      text-color="#ff9900"
      score-template="{value}">
    </el-rate>
    <router-view/>
  </div>
  
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      value1: true,
      value2: 2,
      value3: 3,
      value4: null,
      value5: 4
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
