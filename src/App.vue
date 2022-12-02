<script setup lang="ts">
import IconAccountBox from '~icons/mdi/account-box'
import { useDark, useToggle } from '@vueuse/core'
import HelloWorld from './components/HelloWorld.vue';
const isDark = useDark()
const toggleDark = useToggle(isDark)
</script>

<template>
  <el-row class="mb-4">
    <!-- auto import icon -->
    <i-mdi-cog style="font-size: 2em; color: gray"></i-mdi-cog>
    <!-- import icon -->
    <icon-account-box style="font-size: 2em; color: red" />
    <el-button @click="toggleDark()">切换主题</el-button>
    <el-button type="primary">Primary</el-button>
    <el-button type="success">Success</el-button>
    <el-button type="info">Info</el-button>
    <el-button type="warning">Warning</el-button>
    <el-button type="danger">Danger</el-button>   
  </el-row>
  <HelloWorld :msg="'hello'"/>
</template>

<style scoped>

</style>
