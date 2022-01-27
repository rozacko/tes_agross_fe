<template>
  <div class="row">
    <div class="col-md-12">
      <div class="jumbotron">
        <h1 class="display-4" style="color:white;">Selamat datang, Kerabat!</h1>
        <p class="lead" style="color:white;">Kami hadir dengan membawakan solusi terbaik untuk kebutuhan logistik Anda. Melayani dengan sepenuh hati untuk kenyaman Anda dan keamanan barang sampai pada tujuan. Silakan melakukan pendaftaran untuk dapat menikmati layanan kami.</p>        
        <p class="lead">
          <router-link to="/login" class="btn btn-outline-light" tag="button" style="color:white;">Masuk</router-link>&nbsp;
          <router-link to="/register" class="btn btn-light" tag="button" style="color:green;">Daftar</router-link>
        </p>
      </div>
    </div>
    <div class="col-md-12" style="padding-top:50px">
      <div>
        <b><h2>Mengenal AGROS Indonesia Lebih Dekat</h2></b>
        <p class="lead">Agros adalah sistem terpadu satu pintu - one stop service yang berfokus pada pelayanan jasa logistik muatan berat. Agros menawarkan mitra terlatih, efisiensi dan transparansi sistem transportasi, kemudahan akses untuk layanan pemeliharaan hingga fitur transaksi. </p>
      </div>
    </div>
    <div class="col-md-12" style="padding-top:50px">
      <div>
        <b><h2>Layanan AGROS Indonesia</h2></b>
        <div class="row">
          <div class="col-sm-4">
            <div class="card" style="height: 350px;">
              <img alt="Vue logo" src="../assets/1.png" class="card-img-top">
              <div class="card-body">                
                <h5 class="card-title">AGROS Shipper</h5>
                <p class="card-text">Agros adalah sistem terpadu satu pintu-one stop service yang berfokus pada pelayanan jasa logistik muatan berat. Agros menawarkan mitra terlatih, efisiensi dan </p>
              </div>
            </div>
          </div>
          <div class="col-sm-4">
            <div class="card" style="height: 350px;">
              <img alt="Vue logo" src="../assets/2.png" class="card-img-top">
              <div class="card-body">                
                <h5 class="card-title">AGROS Transporter</h5>
                <p class="card-text">Tidak ada yang tidak mungkin. Kini, Perusahaan bisa dengan cepat mendapatkan keuntungan tanpa harus melakukan hal berat.</p>
              </div>
            </div>
          </div>
          <div class="col-sm-4">
            <div class="card" style="height: 350px;">
              <img alt="Vue logo" src="../assets/3.png" class="card-img-top">
              <div class="card-body">                
                <h5 class="card-title">AGROS Driver</h5>
                <p class="card-text">AGROS menawarkan keleluasaan untuk memilih proyek sehingga peningkatan pendapatan bukan lagi jadi impian.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="col-md-12" style="padding-top:50px">
      <div>
        <b><h2>Cerita Kerabat AGROS</h2></b>
        <div class="row">
          <div class="col-sm-6">
              <img alt="Vue logo" src="../assets/4.png">              
          </div>
          <div class="col-sm-6">
            <p class="card-text" style="margin: auto;padding: 100px 0;">Terinspirasi dari arah mata angin yang membawa pada satu destinasi, Agros akan terus bergerak menciptakan pemerataan ekonomi sehingga bisa menjadi penghubung para stakeholders dalam aktivitas muatan berat, mulai dari shipper, transporter, driver, mitra pemeliharan, seller dan buyer intermoda yang menjangkau seluruh penjuru Nusantara.</p>            
          </div>
        </div>
      </div>
    </div>
    <div class="col-md-12" style="padding-top:50px;padding-bottom:150px">
      <div>
        <b><h2>Mitra AGROS</h2></b>
        <p>Kami berusaha semaksimal mungkin untuk memberikan kenyamanan dan keamanan kepada para pelanggan setia AGROS Indonesia. Untuk melihat daftar pelanggan kami, silakan melakukan pendaftaran.</p>
        <center><router-link to="/register" class="btn btn-success" tag="button" style="color:white;">Gabung Sekarang</router-link></center>
      </div>
    </div>    
  </div>  
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
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
.jumbotron {
  background-image: url("../assets/AGROS_PATT1.png");
  background-size: cover;
}
</style>
