<template>
  <div class="hello">
  <input type="text" v-model="namaDepan">
    <p>nama Saya : {{namaDepan}} <span v-html="namaBelakang"></span></p>
    <p>Umur : {{umur+5}} Tahun</p>
    <p>Status Saya {{status? 'jomlo':'singel'}}</p>
    <p>saya
      <span v-if="umur < 10">Masih unyuk</span>
      <span v-else-if="umur <20">Masih ABG</span>
      <span v-else-if="umur <30">dewasa</span>
      <span v-else>kolot</span><br><br>
      <a v-bind:href="alamat" v-bind:title="umur">Facebook</a>
    </p>
    <ul v-for="Daftar in daftarFakultas ">
    <li >
      Daftar Fakultas {{Daftar.nama}} umur {{Daftar.umur}}
    </li>
    </ul>
    <button @click="sapa(' Selamat Datang')"> Klik Bro</button>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      namaDepan: "Erwin",
      namaBelakang: "<b>SLAM</b>",
      umur: 21,
      status: true,
      alamat: "https://www.facebook.com/",
      daftarFakultas: [
        { nama: "if", umur: 21 },
        { nama: "tl", umur: 21 },
        { nama: "tp", umur: 21 }
      ]
    };
  },
  methods: {
    sapa: function(text) {
      alert("hallo" + text);
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
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
