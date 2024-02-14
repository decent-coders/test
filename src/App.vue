<template>
  <!-- <div class="text-center p">
    <h1>Welcome!</h1>
  </div>
  <div class="p mt-3"><author></author></div>
  <!--   // component + props -->
  <!-- <div class="p mt-3 p-3 d-flex flex-wrap abc">
    <theCard
      v-for="contact in contacts"
      :key="contact.header"
      :Title="contact.title"
      :Header="contact.header"
    ></theCard>
  </div> -->
  <!--   // component + props -->
  <!-- slot -->
  <!-- <div class="p mt-3 p-3 d-flex flex-wrap abc">
    <slots Button="Button1" CardTitle="Card Tittle 1">
      <template #default>
        <img
          src="./components/images/a_logo_for_my_house_named_hawladars (2).jpg"
          class="card-img-top"
          alt="..."
        />
      </template>
      <template #footer>
        <a class="text-center" href="https//www.facebook.com">
          <h1>Facebook</h1>
        </a>
      </template>
    </slots>
    <slots Button="Button2" CardTitle="Card Tittle 2">
      <template #default>
        <a class="text-center" href="https//www.facebook.com">
          <h1>Facebook</h1>
        </a>
      </template>
      <template #footer>
        <img
          src="./components/images/a_logo_for_my_house_named_hawladars (2).jpg"
          class="card-img-top"
          alt="..."
        />
      </template>
    </slots>
    <slots Button="Button3" CardTitle="Card Tittle 3">
      <img
        class="w-75 ms-4"
        src="./components/images/a_logo_for_my_web_development_company_named_Dece.jpg"
        alt=""
      />
    </slots>
  </div> -->

  <div class="p mt-3 p-3 d-flex flex-wrap abc">
    <cards
      v-for="product in products"
      :key="product.name"
      :product="product"
      @buyNowClicked="byNow"
      @addCartClicked="addNow"
      @toggler="toggle"
    ></cards>
  </div>
</template>

<script>
  // // component + props
  // import author from "./components/author.vue";
  // // component + props
  // import theCard from "./components/theCard.vue";
  // // slots + props
  // import slots from "./components/slots.vue";
  //emit + props
  import cards from "./components/cartBuy.vue";

  export default {
    data() {
      return {
        // props
        // contacts: [
        //   {
        //     title: "Primary card title1",
        //     header: "Header1",
        //   },
        //   {
        //     title: "Primary card title2",
        //     header: "Header2",
        //   },
        //   {
        //     title: "Primary card title3",
        //     header: "Header3",
        //   },
        // ],
        products: [
          {
            name: "OnePlus 12R",
            thumbnail:
              "https://fdn.gsmarena.com/imgroot/news/24/02/oneplus-12r-india-price-sale-date/inline/-x393/gsmarena_001.jpg",
            Price: "599.99",
            favourite: true,
          },
          {
            name: "Apple iPhone 15 Plus",
            thumbnail:
              "https://fdn2.gsmarena.com/vv/bigpic/apple-iphone-15-plus-.jpg",
            Price: "1399.99",
            favourite: false,
          },
          {
            name: "Apple iPhone 15",
            thumbnail:
              "https://fdn2.gsmarena.com/vv/bigpic/apple-iphone-15.jpg",
            Price: "999.99",
            favourite: true,
          },
        ],
      };
    },
    methods: {
      byNow(product) {
        console.log(product);
      },
      addNow(product) {
        console.log(product);
      },
      toggle(product) {
        product.favourite = !product.favourite;
      },
    },
    // props
    // components
    components: {
      // author,
      // theCard,
      // slots,
      cards,
    },
    // components
  };
</script>

<style scoped>
  .abc {
    justify-content: space-around;
  }
</style>
