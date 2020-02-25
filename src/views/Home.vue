<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld :msg="showAge()" />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import HelloWorld from "@/components/HelloWorld.vue";

export default Vue.extend({
  name: "Home",
  components: {
    HelloWorld
  },
  data() {
    return {
      age: 123
    };
  },
  computed: {
    test() {
      return this.age;
    }
  },
  methods: {
    showAge() {
      return this.test;
    }
  }
});
</script>
