<script setup lang="ts">
import DefaultTheme from 'vitepress/theme'

const { Layout } = DefaultTheme
</script>

<template>
  <Layout>
    <!-- 全站底部备案栏：在每个页面最下方展示 ICP 备案号并链接到工信部 -->
    <template #layout-bottom>
      <div class="icp-bar">
        <a
          href="https://beian.miit.gov.cn"
          target="_blank"
          rel="noopener noreferrer"
        >蜀ICP备2023021309号</a>
      </div>
    </template>
  </Layout>
</template>

<style scoped>
.icp-bar {
  border-top: 1px solid var(--vp-c-divider);
  padding: 16px 24px;
  text-align: center;
  font-size: 13px;
  line-height: 1.6;
}

.icp-bar a {
  display: inline-flex;
  align-items: center;
  gap: 6px;
  color: var(--vp-c-text-3);
  text-decoration: none;
  transition: color 0.25s;
}

.icp-bar a:hover {
  color: var(--vp-c-brand-1);
}
</style>
