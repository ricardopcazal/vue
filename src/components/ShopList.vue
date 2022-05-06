<template>
  <div class="item_list">
    <h1>Hello ShopList</h1>
    <h1>{{ shopListItem.length }}</h1>
    <span>Items en el carrito</span>
    <form class="form" @submit.prevent="createItem">
      <label for="price">
        Precio de nuectro producto:
        <input id="price" type="text" class="input" v-model="price" />
      </label>

      <label for="text">
        Descripcion de producto
        <input id="text" type="text" class="input" v-model="text" />
      </label>
      <input type="submit" value="Agregar al carrito" class="button" />
    </form>
    <br />
    <ul>
      <li v-for="(item, index) in shopListItem" v-bind:key="index">
        <div>
          <p>{{ item.text }}</p>
          <span>{{ item.price }}</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ShopList",
  data: function () {
    return {
      text: "",
      price: 0,
      shopListItem: [],
      total: 0,
    };
  },
  methods: {
    createItem() {
      console.log("hola");
      const item = {
        id: this.shopListItem.length + 1,
        price: this.price,
        text: this.text,
        completed: false,
      };

      this.shopListItem.push(item);
      this.price = 0;
      this.text = "";
    },
  },
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
