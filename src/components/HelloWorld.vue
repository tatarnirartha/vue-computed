<template>
  <div class="hello">
    <h3>Jumlah :</h3>
    <input type="number" placeholder="Jumlah" v-model="jumlah">
    <h3>Harga : </h3>
    <input type="number" placeholder="Harga" v-model="harga">
    <h3>Diskon % :</h3>
    <input type="number" placeholder="Diskon %" v-model="diskon">
    <h5>Total</h5>
    <h6>{{getTotal}}</h6>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      jumlah: 0,
      harga: 0,
      diskon: 0
    }
  },
  computed: {
    getTotal(){
      const a = this.jumlah * this.harga
      return a - (a * (this.diskon / 100))
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
