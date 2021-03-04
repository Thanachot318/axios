<template>
  <div class="home">
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    <b-img
      src="https://www.prachachat.net/wp-content/uploads/2018/09/%E0%B8%81.%E0%B8%A5.%E0%B8%95..jpeg"
    />
    <HelloWorld msg="Welcome to SEC" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
};
</script>
