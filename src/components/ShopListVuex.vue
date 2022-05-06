<template>
  <h1>Helo ShopLitVuex</h1>
</template>

<script>
export default {
  name: "ShopListVuex",
};
</script>

<style scoped>
.item-list {
  width: 800px;
  max-width: 100%;
  margin: 0px auto;
}

.form {
  background: white;
  border-radius: 12px;
  padding: 30px;
  box-shadow: 0px 10px 22px -1px rgba(0, 0, 0, 0.25);
  margin-top: 10px;
}

.label {
  display: block;
  margin-bottom: 10px;
}

.input {
  height: 35px;
}

.button {
  margin-left: 20px;
  height: 35px;
  border: none;
  border-radius: 5px;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.2);
  background-color: #2ecc71;
  color: #ecf0f1;
  cursor: pointer;
}

.list {
  margin-top: 40px;
}

.item {
  cursor: pointer;
  margin: 10px 0;
}

.completed {
  text-decoration: line-through;
  color: lightgrey;
}
</style>
