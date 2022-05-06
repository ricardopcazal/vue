<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <ShopList />
  </div>
</template>

<script>
// @ is an alias to /src
import ShopList from "@/components/ShopList";
export default {
  name: "HomeView",
  components: {
    ShopList,
  },
};
</script>
