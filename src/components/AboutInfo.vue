<template>
  <div>
    <a-rate v-model:value="value1" allowHalf>
      <template #character>
        <heart-outlined />
      </template>
    </a-rate>
    <span class="ant-rate-text">Rating your experience</span>
  </div>
</template>
<script lang="ts">
import { HeartOutlined } from '@ant-design/icons-vue';
import { defineComponent, ref } from 'vue';
export default defineComponent({
  setup() {
    const value1 = ref<number>(5);
    return {
      value1,
    };
  },
  components: {
    HeartOutlined,
  },
});
</script>

