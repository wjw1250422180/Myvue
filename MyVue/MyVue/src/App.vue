<template>
  <div id="app">
    <HelloWorld></HelloWorld>
  </div>
</template>


<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue' //导入组件

export default {
  name: 'app',
  components: {
    //注册组件
    HelloWorld: HelloWorld
  }
}
</script>