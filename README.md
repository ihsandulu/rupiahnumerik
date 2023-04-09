# rupiahnumerik

Fungsi isi dibuat untuk memecah ribuan otomatis pada inputan angka untuk ditampilkan pada user, dan mengembalikan format awal (yaitu tanpa koma dan titik sebagai pemisah desimal) ketika melempar ke database.

Terimakasih pada pembuat fungsi number_format (http://kevin.vanzonneveld.net).

Terimakasih pada pembuat fungsi formatRupiah (https://www.malasngoding.com/membuat-format-rupiah-dengan-javascript/).

Anda hanya perlu memasukkan fungsi ini [rupiahnumerik(this)] pada onkeyup di elemen input.

Jika elemen input bertipe selain text maka akan otomatis dirubah menjadi bertipe text.

Hasil post tetap akan melemparkan angka yg dapat diterima oleh database (yaitu tanpa koma dan titik sebagai pemisah desimal).

PENTING :

1. Wajib mengisi id pada elemen input.
2. Id dan name wajib sama penamaannya.
3. Tambahkan attribut onkeyup pada elemen input : onkeyup="rupiahnumerik(this);"
4. Tambahkan script : <script>rupiahnumerik($("#idnya"))</script>
5. Type pada database harus text.
6. Membutuhkan Jquery.
7. Letakkan Event Attribute (baik untuk onchange, onkeyup atau lainnya) di attribute "change".

---

Contoh:

<input onkeyup="rupiahnumerik(this);" change="alert();" type="number" id="idnya" name="idnya"\>

<script>rupiahnumerik($("#idnya"));</script>

---

Memasukkan Nilai via function lain ke dalam inputan/field:

'<select required onchange="isi(); selisih();" class="form-control select" id="product_id" name="product_id">
<option value="" disabled>Pilih Produk</option>
<option value="3" stok="40">Semen 3 Roda</option>
</select>

<input onkeyup="rupiahnumerik(this);" change="alert();" type="number" id="idnya" name="idnya"\>

<script>rupiahnumerik($("#idnya"));</script><br/>

<script><br/>

    function isi(){<br/>

        let productid = $("#product_id option:selected");<br/>

        let stok = productid.attr("stok");<br/>

        $("#idnya").val(stok);<br/>

        //tuliskan fungsi rupiahnumerik disini!!!<br/>

        rupiahnumerik($("#idnya"));<br/>
    }<br/>

</script>

---

Pembuat Fungsi 'rupiahnumerik': ihsandulu (https://www.qithy.com)

Catatan: Silahkan merubah sourcecode tanpa menghilangkan catatan ini.
