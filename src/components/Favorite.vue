<script>
  export default {
    props: {
        favs: {
            type: Array,
            required: true
        },
        getFromFavs: {
            type: Function,
            required: true
        }
    }
  }
</script>


<template>
  <h2>Choose your favorites</h2>
  <div @click="getFromFavs(index)" v-for="(el, index) in favs" :key="index">
    <span>{{ el.from }}</span>
    <span>{{ el.to }}</span>
  </div>
</template>


<style scoped>
h2 {
    color: #fff;
    font-family: 'Calibri';
}
div {
    display: flex;
    justify-content: space-between;
    width: 150px;
    margin: 10px auto;
    transition: all 500ms ease;
}
div:hover {
    opacity: 0.7;
    transform: scale(1.1);
    cursor: pointer;
}
span {
    font-family: 'Calibri';
    padding: 10px 15px;
    background: #8c00ff;
    color: #fff;
}
</style>