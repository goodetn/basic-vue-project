<script lang="ts">
import { defineComponent, ref } from 'vue';
import { RouterLink, RouterView } from "vue-router";

import "ant-design-vue/dist/antd.css";

export default defineComponent({
  setup() {
    return {
      selectedKeys: ref<string[]>(['1']),
    };
  },
});
</script>

<template>
  <a-layout>
    <a-layout-header :style="{ position: 'fixed', zIndex: 1, width: '100%' }">
      <div class="logo" />
      <a-menu theme="dark" mode="horizontal" v-model:selectedKeys="selectedKeys" :style="{ lineHeight: '64px' }">
        <a-menu-item key="1">
          <RouterLink to="/">Home</RouterLink>
        </a-menu-item>
        <a-menu-item key="2">
          <RouterLink to="/about">About</RouterLink>
        </a-menu-item>
        <a-menu-item key="3">
          <RouterLink to="/customer">Customer</RouterLink>
        </a-menu-item>
        <a-menu-item key="4">
          <RouterLink to="/contact">Contact</RouterLink>
        </a-menu-item>
      </a-menu>
    </a-layout-header>
    <a-layout-content :style="{ padding: '0 50px', marginTop: '64px' }">
      <Header />
      <div :style="{ background: '#fff', padding: '24px', minHeight: '380px' }">
        <RouterView />
      </div>
    </a-layout-content>
    <a-layout-footer :style="{ textAlign: 'center' }">
      Ant Design ©2018 Created by Ant UED
    </a-layout-footer>
  </a-layout>
</template>

<style>
#components-layout-demo-fixed .logo {
  width: 120px;
  height: 31px;
  background: rgba(229, 26, 26, 0.2);
  margin: 16px 24px 16px 0;
  float: left;
}

.site-layout .site-layout-background {
  background: #fff;
}

[data-theme='dark'] .site-layout .site-layout-background {
  background: #141414;
}
</style>
