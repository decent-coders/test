<template lang="">
  <div>
    <div class="card" style="width: 18rem">
      <h5 class="card-title p-2 m-0 text-bg-secondary text-center">
        {{ CardTitle }}
      </h5>
      <div class="card-body">
        <slot></slot>
        <p class="card-text">
          Some quick example text to build on the card title and make up the
          bulk of the card's content.
        </p>
        <h5 class="card-title p-2 m-0 text-bg-light text-center">
          <slot name="footer" v-if="$slots.footer"></slot>
        </h5>
        <a href="#" class="btn btn-primary">{{ Button }}</a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    props: ["CardTitle", "Button"],
  };
</script>

<style></style>
