<template>
  <div>
    <HelloWorld msg="Vue3示例"></HelloWorld>
    <div class="content" style="text-align: center">
      <p :class="cls">
        当前vue版本
        <el-tag style="vertical-align: text-top" size="small">3.2.24</el-tag>
      </p>
      <p>
        当前element版本
        <el-tag style="vertical-align: text-top" size="small">2.2.6</el-tag>
      </p>
      <p>
        当前ant-design-vue版本
        <el-tag style="vertical-align: text-top" size="small">2.2.8</el-tag>
      </p>
      <p>
        <el-button @click="() => open('https://github.com/Tencent/wujie/tree/master/examples/vue3')"
          >仓库地址</el-button
        >
      </p>
    </div>
  </div>
</template>

<script>
import HelloWorld from "@/components/HelloWorld.vue";
import { tw, apply } from 'twind';


// cls 是 使用twind 生成的样式，首次加载时是生效的，样式是 文本红色，padding 16px，文字放大。
// 同一个应用切换到别的路由，再切回来样式就没了

export default {
  data() {
    return {
      open: window.open,
      cls: tw`${apply`text-red-500 p-4 text-lg`}`
    };
  },
  components: {
    HelloWorld,
  },
};
</script>

<style>
:root {
  --host-color: #f16b5f;
}
</style>
