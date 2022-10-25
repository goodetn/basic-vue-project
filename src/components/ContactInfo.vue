<template>
  <a-result status="success" title="Great, we have done all the operations!">
    <template #extra>
      <a-button key="console" type="primary">Go Console</a-button>
      <a-button key="buy">Buy Again</a-button>
      <MessageInfo />
    </template>

    <div class="desc">
      <p style="font-size: 16px">
        <strong>The content you submitted has the following error:</strong>
      </p>
      <p>
        <check-circle-outlined :style="{ color: 'green' }" />
        Your account has been frozen
        <a>Thaw immediately &gt;</a>
      </p>
      <p>
        <check-circle-outlined :style="{ color: 'green' }" />
        Your account is not yet eligible to apply
        <a>Apply Unlock &gt;</a>
      </p>
    </div>
  </a-result>
</template>
<script lang="ts">
import { CheckCircleOutlined } from '@ant-design/icons-vue';
import { defineComponent } from 'vue';
import MessageInfo from './MessageInfo.vue';
export default defineComponent({
  components: {
    CheckCircleOutlined,
    MessageInfo,
},
});
</script>
<style scoped>
.desc p {
  margin-bottom: 1em;
}
</style>
