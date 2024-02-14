<template lang="">
  <div>
    <div class="card text-center" style="width: 18rem">
      <h5 class="card-title p-2 m-0 text-bg-secondary text-start">
        {{ product.name }}
        <img
          class="me-2"
          src="./images/lover.png"
          alt=""
          v-if="product.favourite"
          @click="toggle"
        />
        <img
          class="me-2"
          src="./images/heart.png"
          alt=""
          v-else
          @click="toggle"
        />
      </h5>
      <div class="card-body">
        <img :src="product.thumbnail" alt="" class="w-50" />
        <h5 class="card-title p-2 m-0 text-center">{{ product.Price }}$</h5>
        <a class="btn btn-success me-4" @click="buyHandle">Buy now</a>
        <a class="btn btn-warning ms-5" @click="cartHandle">Add cart</a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    // emits: {
    //   buyNowClicked: function (data) {
    //     if (!data) {
    //       console.log("data missing");
    //       return false;
    //     }
    //     return true;
    //   },
    // },
    props: { product: { type: Object, default: () => ({}) } },
    data() {
      return {};
    },
    methods: {
      buyHandle() {
        this.$emit("buyNowClicked", this.product.name);
      },
      cartHandle() {
        this.$emit("addCartClicked", this.product.Price);
      },
      toggle() {
        this.$emit("toggler", this.product);
      },
    },
  };
</script>

<style>
  .card-title img {
    width: 21px;
    vertical-align: middle;
    float: right;
  }
</style>
