<template>
  <div class="about">
    <shop-list-vuex />
  </div>
</template>
<script>
import shopListVuex from "@/components/ShopListVuex";

export default {
  name: "AboutView",
  components: {
    shopListVuex,
  },
};
</script>
