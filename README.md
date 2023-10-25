# Cara Membuat Form HTML dengan Validasi **JavaScript** di HTML 
-  Terdapat 3 inputan didalam form, yaitu:

## 1. Membuat Form Nama
Saya akan memberikan Validasi berupa inputan hanya boleh menggunakan *Huruf/Alphabet* saja.
```
<!-- fungsi alphabet -->
function Alphabet(nilai, pesan) {
  var alphaExp = /^[a-zA-Z]+$/;
  if(nilai.value.match(alphaExp)) {
    return true;
  }
  else {
    alert(pesan);
    nilai.focus();
    return false;
  }
}
```
#### Penjelasan
- Pertama membuat nama function Alphabet, dengan parameter dinamis, yaitu(nilai, pesan).
- Data yang boleh dimasukkan adalah berupa "**a-zA-Z**".
- Jika selain data "**a-zA-Z**" ini dimasukkan, maka akan muncul pesan alert"**alert(pesan)**".
<img width="731" alt="image" src="https://github.com/sayaveni04/praktikum_PemWeb5/assets/115862597/48f8f974-5a96-4b8f-94bb-37428eb09880">

## 2. No. Telp
Pada bagian ini akan saya berikan validasi berupa hanya *nomor/angka* saja yang boleh diinputkan.
```
<!-- fungsi number -->
            function Number(nilai, pesan) {
                var numberExp = /^[0-9]+$/;
                if(nilai.value.match(numberExp)) {
                    return true;
                }
                else {
                    alert(pesan);
                    nilai.focus();
                    return false;
                }
            }
            <!-- fungsi Email  -->
            function cekEmail(nilai, pesan) {
                var email = /^([a-zA-Z0-9_.+-])+@(([a-zA-Z0-9-])+.)+([a-zA-Z0-9]{2,4})+$/;
                if(nilai.value.match(email)) {
                    return true;
                }
                else {
                    alert(pesan);
                    nilai.focus();
                    return false;
                }
            }
```
#### Penjelasan  :
- var numberExp = /^[0-9]+$/; merupakan variabel **numberExp** yang diberi batasan validasi angka 0-9.
- Arti **Match** pada "if(nilai.value.match(numberExp))" adalah *string.match()*, mencari string menggunakan Regular Expression (Regex).
- Jika salah atau inputan tidak benak maka akan ada pesan alert"**alert(pesan)"**
<img width="728" alt="image" src="https://github.com/sayaveni04/praktikum_PemWeb5/assets/115862597/ac8e87ae-4db3-4920-a38d-0aaea1ec5bbf">

## 3. Email
Pada email akan diberikan validasi masih berupa *Regular Expression*.
```
 <!-- fungsi Email  -->
            function cekEmail(nilai, pesan) {
                var email = /^([a-zA-Z0-9_.+-])+@(([a-zA-Z0-9-])+.)+([a-zA-Z0-9]{2,4})+$/;
                if(nilai.value.match(email)) {
                    return true;
                }
                else {
                    alert(pesan);
                    nilai.focus();
                    return false;
                }
            }  
```
#### Penjelasan
-  Membuat variabel **email** "var email = /^([a-zA-Z0-9_.+-])+(([a-aZ-Z0-9-])+.)+([a-zA-Z0-9]){2,4})+$/; "berupa huruf, angka dan simbol yang diperbolehkan dalam menginputkan sebuah email.
<img width="728" alt="image" src="https://github.com/sayaveni04/praktikum_PemWeb5/assets/115862597/b98f5884-f892-46f5-a217-8abf0974fe3c">

## 4. Validasi tambahan(pesan)
Validasi ini hanya tambahan yaitu *pesan alert* yang disampaikan setelah inputan dimasukkan.
```
function validasi() {
  Alphabet(document.getElementById('nama'), 'Nama harus Huruf semua!!');
  Number(document.getElementById('telp'), 'Telp. hanya ber isi Number!!');
  cekEmail(document.getElementById('email'), 'Email tidak benar!!');
}
```
#### Penjelasan
-  pada function "*Alphabet*" dengan ID "nama" berupa pesan alert"Nama harus Huruf semua!!"
-  pada function "*Number*" dengan ID "telp" berupa pesan alert"Telp. hanya berisi Number!!"
-  pada function "*cekEmail*" dengan iD "email" berupa pesan alert"Email tidak benar!!"

## Form HTML
```
<form>
            <p>Nama :
            <input type="text" name="nama" id="nama"></p>
            <p>No. Telp :
            <input type="number" name="telp" id="telp"></p>
            <p>Email :
            <input type="email" name="email" id="email"></p>
            <p><input type="submit" onClick="validasi()"           value="Submit"></p>
</form>
```
#### Penjelasan
- Input **Nama**, <input type="text" name="nama" id="nama"> dengan ID "nama".
- Input **No. Telp**, <input type="number" name="telp" id="telp"> dengan ID "telp".
- Input **Email**, <input type="email" name"email" id"email"> dengan ID "email.
- Input type **Sumbit**, <input type="sumbit" onClick="validasi()" value="Sumbit"> untuk mensumbit/mengirim data lebih lanjut, dengan disertai Event JavaScript "*onClick*" dan pemanggilan functiom bernama "*validasi()*".
<img width="730" alt="image" src="https://github.com/sayaveni04/praktikum_PemWeb5/assets/115862597/f77c3077-0bd6-4edd-9b3d-072a00a64051">
