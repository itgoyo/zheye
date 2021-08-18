<template>
  <div class="container">
    <global-header :user="currentUser"></global-header>
    <column-list :list="list"></column-list>
  </div>
</template>
<script lang="ts">

import { defineComponent } from 'vue'
import 'bootstrap/dist/css/bootstrap.min.css'
import ColumnList, { ColumnProps } from './components/ColumnList.vue'
import GlobalHeader, { UserProps } from './components/GlobalHeader.vue'
const currentUser: UserProps = {
  isLogin: false
}
const testData: ColumnProps[] = [
  {
    id: 1,
    title: 'test1的专栏',
    description: '这是一篇test1的专栏',
    avatar: 'https://avatars.githubusercontent.com/u/23348551?s=60&v=4'
  },
  {
    id: 2,
    title: 'test2的专栏',
    description: '这是一篇test1的专栏',
    avatar: 'https://avatars.githubusercontent.com/u/23348551?s=60&v=4'
  },
  {
    id: 3,
    title: 'test的专栏',
    description: '这是一篇test1的专栏'
    // avatar: 'https://avatars.githubusercontent.com/u/23348551?s=60&v=4'
  },
  {
    id: 4,
    title: 'test1的专栏',
    description: '这是一篇test1的专栏',
    avatar: 'https://avatars.githubusercontent.com/u/23348551?s=60&v=4'
  }
]

export default defineComponent({
  name: 'App',
  components: {
    ColumnList,
    GlobalHeader
  },
  setup () {
    return {
      list: testData,
      currentUser

    }
  }
})
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
