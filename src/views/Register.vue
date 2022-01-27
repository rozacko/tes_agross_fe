//register.vue
<template>
  <div class="row justify-content-md-center">
    <div class="col-md-12">
      <div class="card">        
        <div class="card-body">
            <h1><b>Daftar Sekarang</b></h1>
            <p>Mari bergabung bersama Kerabat AGROS Indonesia lainnya.</p>
            <form>
            <div class="row">                
                <div class="col-md-6">
                        <div class="form-group">
                            <label for="name">Nama Lengkap Kerabat</label>
                            <input type="text" class="form-control" placeholder="Contoh : Bambang" />
                        </div>
                        <div class="form-group">
                            <label for="email">Email</label>
                            <input type="text" class="form-control" placeholder="Contoh: bambang@gmail.com" />
                        </div>
                        <div class="form-group">
                            <label for="role">Role</label>
                            <label for="sel1">Select list:</label>
                            <select class="form-control" id="sel1">
                                <option value="1">Super Admin</option>                                
                                <option value="2">Customer</option>                                
                            </select>                            
                        </div>
                        <button type="submit" class="btn btn-success">Gabung Sekarang</button>
                </div>
                <div class="col-md-6">
                        <div class="form-group">
                            <label for="kota">Asal Kota</label>
                            <input type="text" class="form-control" placeholder="Contoh : Pekalongan" />
                        </div>
                        <div class="form-group">
                            <label for="password">Password</label>
                            <input type="password" class="form-control" placeholder="" />
                        </div>
                </div>                
            </div>    
            </form>      
        </div>
      </div>
    </div>
    <div class="col-md-12" style="padding-top:50px;padding-botton:150px">
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
  </div>
</template>
