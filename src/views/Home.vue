<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld :msg="showAge()" />
  </div>
</template>

<script lang="ts">
import { defineComponent, reactive, computed } from "@vue/composition-api";
import HelloWorld, { HelloWorldProps } from "@/components/HelloWorld.vue";

export default defineComponent({
  name: "Home",
  components: {
    HelloWorld
  },
  setup() {
    const data = reactive({ age: 123 });
    const test = computed(() => data.age);
    const showAge = () => test.value;
    return {
      showAge
    };
  }
});
</script>
