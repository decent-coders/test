<template lang="">
    <div class='d-flex flex-wrap abc'>
        <div class="card text-bg-primary mb-3" style="max-width: 18rem;">
          <div class="card-header">{{Header}}</div>
            <div class="card-body">
                <h5 class="card-title">{{Title}}</h5>
                <p class="card-text">Some quick example text to build on the card title and make up the bulk of the card's content.</p>
            </div>
        </div>
    </div>
</template>


<script>

export default {
    props:['Header', 'Title'],
}
</script>

<style scoped>

</style>