<template>
  <div id="app">
    <sidebar id="sidebar" />
    <router-view id="router" :key="$router.path" />
  </div>
</template>
<script lang="ts">
import { defineComponent } from "vue";
import sidebar from "./views/Sidebar.vue";
export default defineComponent({
  components: { sidebar }
});
</script>

<style scoped>
#app {
  border: #2c3e50;
  display: flex;
}
#sidebar{
  border: red;
}
#router{
  border: red;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
