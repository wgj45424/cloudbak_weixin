<script setup>
import {useStore} from "vuex";

const store = useStore();
</script>

<template>
  <div class="s-page">
    <div class="page-body">
      <div class="conf-group">
        <div class="conf-title">系统信息</div>
        <div class="conf-row">
          <div class="conf-label">系统版本</div>
          <div class="conf-right">
            <p>{{store.getters.getSysInfo?.sys_version}}</p>
          </div>
        </div>
        <div class="conf-row">
          <div class="conf-label">系统唯一标识</div>
          <div class="conf-right">
            {{ store.getters.getSysInfo.client_id }}
          </div>
        </div>
      </div>
    </div>
  </div>

</template>

<style scoped lang="less">
@import "/src/style/components/tools/tab.less";
</style>
