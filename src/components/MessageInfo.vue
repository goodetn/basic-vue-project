<template>
  <a-button @click="success">Testing Message, disappear in 5 seconds</a-button>
</template>
<script lang="ts">
import { message } from 'ant-design-vue';
import { defineComponent } from 'vue';
export default defineComponent({
  setup() {
    const success = () => {
      message.success(
        'Testing Message of setting project, and it will disappear in 5 seconds',
        5,
      );
    };
    return {
      success,
    };
  },
});
</script>

