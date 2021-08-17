<template>
  <div class="container">
    <column-list :list="list"></column-list>
  </div>
</template>
<script lang="ts">

import { defineComponent } from 'vue'
import 'bootstrap/dist/css/bootstrap.min.css'
import ColumnList, { ColumnProps } from './components/ColumnList.vue'

const testData: ColumnProps[] = [
  {
    id: 1,
    title: 'test1的专栏',
    description: '这是一篇test1的专栏',
    avatar: 'https://exp-picture.cdn.bcebos.com/fdb4f00d3aceaad797bdfb56eee7340f6578b86f.jpg?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_500%2Climit_1%2Fformat%2Cf_jpg%2Fquality%2Cq_80'
  },
  {
    id: 2,
    title: 'test2的专栏',
    description: '这是一篇test1的专栏',
    avatar: 'https://exp-picture.cdn.bcebos.com/fdb4f00d3aceaad797bdfb56eee7340f6578b86f.jpg?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_500%2Climit_1%2Fformat%2Cf_jpg%2Fquality%2Cq_80'
  },
  {
    id: 3,
    title: 'test的专栏',
    description: '这是一篇test1的专栏',
    avatar: 'https://exp-picture.cdn.bcebos.com/fdb4f00d3aceaad797bdfb56eee7340f6578b86f.jpg?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_500%2Climit_1%2Fformat%2Cf_jpg%2Fquality%2Cq_80'
  },
  {
    id: 4,
    title: 'test1的专栏',
    description: '这是一篇test1的专栏',
    avatar: 'https://exp-picture.cdn.bcebos.com/fdb4f00d3aceaad797bdfb56eee7340f6578b86f.jpg?x-bce-process=image%2Fresize%2Cm_lfit%2Cw_500%2Climit_1%2Fformat%2Cf_jpg%2Fquality%2Cq_80'
  }
]

export default defineComponent({
  name: 'App',
  components: {
    ColumnList
  },
  setup () {
    return {
      list: testData
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
