# rupiahnumerik

Fungsi isi dibuat untuk memecah ribuan otomatis pada inputan angka untuk ditampilkan pada user, dan mengembalikan format awal (yaitu tanpa koma dan titik sebagai pemisah desimal) ketika melempar ke database.

Terimakasih pada pembuat fungsi number_format (http://kevin.vanzonneveld.net)
Terimakasih pada pembuat fungsi formatRupiah (https://www.malasngoding.com/membuat-format-rupiah-dengan-javascript/)

Anda hanya perlu memasukkan fungsi ini [rupiahnumerik(this)] pada onkeyup di elemen input.
Jika elemen input bertipe selain text maka akan otomatis dirubah menjadi bertipe text.
Hasil post tetap akan melemparkan angka yg dapat diterima oleh database (yaitu tanpa koma dan titik sebagai pemisah desimal).
Perhatian : Wajib mengisi id pada elemen input.
Perhatian : Membutuhkan Jquery.

Contoh:

<input onkeyup="rupiahnumerik(this);" type="number" id="isian" name="isian"//>

<script>rupiahnumerik($("#request1_proposed_nom"))</script>

Pembuat Fungsi 'rupiahnumerik': ihsandulu (https://www.qithy.com)
Catatan: Silahkan merubah sourcecode tanpa menghilangkan catatan ini.
