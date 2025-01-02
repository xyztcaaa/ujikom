<template>
    <div class="container">
        <h1 class="judul" style="text-align: center;">Identitas SMKN 4 TASIKMALAYA</h1>
        <div class="card shadow small mt-5">
            <table class="table m-3">
                <tr>
                    <td colspan="3" class="logo-cell">
                        <img src="~/assets/img/logo.png" alt="Logo SMKN 4 Tasikmalaya" class="logo">
                    </td>
                </tr>
                <tr>
                    <td>Nama Sekolah</td>
                    <td>:</td>
                    <td>SMK Negeri 4 Kota Tasikmalaya</td>
                </tr>
                <tr>
                    <td>NPSN</td>
                    <td>:</td>
                    <td>20276063</td>
                </tr>
                <tr>
                    <td>Alamat</td>
                    <td>:</td>
                    <td>Jl Depok RT 02 RW 05, Kelurahan Sukamenak, Kecamatan Purbaratu, <br> Kota Tasikmalaya, Provinsi Jawabarat</td>
                </tr>
                <tr>
                    <td>Telp/faks</td>
                    <td>:</td>
                    <td>(0265) 7528981</td>
                </tr>
                <tr>
                    <td>Email</td>
                    <td>:</td>
                    <td>info@smkn4-tsm.sch.id</td>
                </tr>
                <tr>
                    <td>Tahun Berdiri/Beroperasi</td>
                    <td>:</td>
                    <td>2010</td>
                </tr>
                <tr>
                    <td>Nomor SK Pendirian</td>
                    <td>:</td>
                    <td>420/9/SK-BPPT/2012</td>
                </tr>
                <tr>
                    <td>Tanggal SK Pendirian</td>
                    <td>:</td>
                    <td>06 Februari 2012</td>
                </tr>
                <tr>
                    <td>Kepemilikan</td>
                    <td>:</td>
                    <td>Pemerintah Daerah</td>
                </tr>
            </table>
        </div>
    </div>
</template>

<script>
useHead({
  title: 'Identitas - SMK Negeri 4 Tasikmalaya',
  meta: [
    {
      name: 'description',
      content: 'Identitas SMK Negeri 4 Tasikmalaya',
    },
  ],
});

</script>
<style scoped>
.judul {
    font-size: 1.7rem;
    font-weight: bold;
    margin-bottom: 2rem;
    color: #333;
    margin-top: 10rem;
}

.table {
    font-family: "Poppins", serif;
    width: 100%;
}

.logo-cell {
    text-align: center;
    padding: 20px 0;
}

.logo {
    width: 120px;
    margin: auto;
}

.small {
    background-color: transparent;
    backdrop-filter: blur(20px);
    border: 2px solid #ffff;
    width: 90%;
    margin: auto;
}

td {
    border-bottom: none;
    padding: 10px;
}

@media only screen and (max-width: 600px) {
    td {
        font-size: small;
        padding: 5px;
    }

    .logo {
        width: 80px;
    }
}
</style>
