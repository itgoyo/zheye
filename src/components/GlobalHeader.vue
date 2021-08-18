<template>
  <nav class="navbar navbar-dark bg-primary justify-content-between mb-4 px-4">
<a class="navbar-brand" to="/">者也专栏</a>
<ul v-if="!user.isLogin">
  <li class="list-inline-item"><a to="/login" class="btn btn-outline-light my-2">登陆</a></li>
  <li class="list-inline-item"><a to="/signup" class="btn btn-outline-light my-2">注册</a></li>
</ul>
<ul v-else class="list-inline mb-0">
  <li class="list-inline-item"><a to="/user" class="btn btn-outline-light my-2">个人中心</a></li>
</ul>



  </nav>

</template>

<script lang="ts">
import { computed, defineComponent, PropType } from 'vue'

export interface UserProps {
  isLogin: boolean;
  name?: string;
  id?: number;
}


export default defineComponent({
  name: 'GlobalHeader',
  props: {
    user: {
      type: Object as PropType<UserProps>,
      required: true
    }
  },
  setup (props) {
  }
})

</script>
