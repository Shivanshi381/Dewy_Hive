<template>
    <v-container fluid class="gradient-background">
      <v-card>
        <v-card-title class="text-center font-weight-black">My Cart</v-card-title>
        <v-divider></v-divider>
        <v-list>
          <v-list-item-group v-model="selected">
            <v-list-item v-for="(item, index) in items" :key="index">
              <v-list-item-avatar>
                <v-img :src="item.image" contain></v-img>
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title>{{ item.name }}</v-list-item-title>
                <v-list-item-subtitle>{{ item.price }}</v-list-item-subtitle>
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon @click="removeItem(index)">
                  <v-icon>mdi-delete</v-icon>
                </v-btn>
              </v-list-item-action>
            </v-list-item>
          </v-list-item-group>
        </v-list>
        <v-divider></v-divider>
        <v-card-text>
          <h3>Address:</h3>
          <v-list v-if="addresses.length > 0">
            <v-list-item-group v-model="selectedAddress">
              <v-list-item v-for="(address, index) in addresses" :key="index">
                <v-list-item-content>
                  <v-list-item-title>{{ address }}</v-list-item-title>
                </v-list-item-content>
                <v-list-item-action>
                  <v-btn icon small @click="editAddress(index)">
                    <v-icon>mdi-pencil</v-icon>
                  </v-btn>
                  <v-btn icon small @click="deleteAddress(index)">
                    <v-icon>mdi-delete</v-icon>
                  </v-btn>
                </v-list-item-action>
              </v-list-item>
            </v-list-item-group>
          </v-list>
          <v-text-field v-model="newAddress" placeholder="Enter your address"></v-text-field>
          <v-btn color="#C51162" @click="addAddress">Add Address</v-btn>
          <v-btn v-if="editingAddress !== null" color="#C51162" @click="updateAddress">Update Address</v-btn>
        </v-card-text>
        <v-card-actions>
          <v-spacer></v-spacer>
          <v-btn color="#C51162" @click="checkout">Checkout</v-btn>
          <v-btn color="#C51162" @click="clearCart">Clear Cart</v-btn>
        </v-card-actions>
      </v-card>
    </v-container>
  </template>
  
  <script>
  export default {
    name: "CartPage",
    data: () => ({
      items: [
        {
          name: "Item 1",
          price: "$10.00",
          image: "/img/1.png",
        },
      ],
      selected: [],
      addresses: [],
      selectedAddress: null,
      newAddress: "",
      editingAddress: null,
    }),
    methods: {
      removeItem(index) {
        this.items.splice(index, 1);
      },
      clearCart() {
        this.items = [];
        this.selected = [];
        this.addresses = [];
        this.selectedAddress = null;
        this.newAddress = "";
        this.editingAddress = null;
      },
      checkout() {
        if (this.selectedAddress !== null) {
          alert(`Checkout successful! Your items will be delivered to ${this.addresses[this.selectedAddress]}`);
        } else {
          alert("Please select an address to deliver your items");
        }
      },
     
  
},
  };

</script>

<style>
.gradient-background {
  background: linear-gradient(to right, #ffffff, #ff69b4);
}
</style>