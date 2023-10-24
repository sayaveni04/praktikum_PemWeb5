# Cara Membuat Form HTML dengan Validasi **JavaScript** di HTML 
-  Terdapat 3 inputan didalam form, yaitu:

## 1. Membuat Form Nama
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
- Pertama membuat nama function Alphabet, dengan parameter dinamis, yaitu(nilai, pesan)
- Data yang boleh dimasukkan adalah berupa "**a-zA-Z**"
- Jika selain data "**a-zA-Z**" ini dimasukkan, 
