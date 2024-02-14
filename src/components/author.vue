<script >
export default {
    data() {
        return {
            
        }
    },
};
</script>

<template>
    <div class='p-3 mt-2 text-center abc'>
        <h3>Hridoy Hawladar</h3>
        <h6>An insanely ambicious man!!</h6>
        <div class="globes d-flex">
          <div class="globe bg-danger"></div>
          <div class="globe mx-4 bg-warning"></div>
          <div class="globe bg-success"></div>
        </div>
    </div>
</template>

<style scoped>
.globe{
  height: 50px;
  width: 50px;
  border-radius: 50%;
  cursor: pointer;
}
.globes{
  justify-content: center;
}
</style>
