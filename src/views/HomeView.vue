<template>
  <div class="home">
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
