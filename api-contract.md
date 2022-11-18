# Agenda XI RPL
##

## Data Siswa XI RPL
<details>
<summary> Klik untuk Ekspan </summary>

### Create Siswa
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/siswa </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> POST </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "nama" : "Ahdi Kal Fatur",
    "nis" : "20.1.1",
    "alamat" : "Bogor",
    "hoby" : "Musik"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Siswa Berhasil diinput",
    "data" : {
        "id" : 001,
        "nama" : "Ahdi Kal Fatur",
        "nis" : "20.1.1",
        "alamat" : "Bogor",
        "hoby" : "Musik"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Siswa Telah digunakan",
    "data" : {
        "value" : "Ahdi Kal Fatur",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>


### Read Siswa By Id
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/siswa </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/siswa?id=001 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=001 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "id" : 001,
        "nama" : "Ahdi Kal Fatur",
        "nis" : "20.1.1",
        "alamat" : "Bogor",
        "hoby" : "Musik"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Siswa tidak ditemukan",
    "data" : {
        "value" : 001,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>


### Read Siswa All
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/siswa </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : [
        {
            "id" : 001,
            "nama" : "Ahdi Kal Fatur",
            "nis" : "20.1.1",
            "alamat" : "Bogor",
            "hoby" : "Musik"
        },
        {
            "id" : 002,
            "nama" : "Bambang Ferdi",
            "nis" : "20.1.2",
            "alamat" : "Bogor",
            "hoby" : "Game"
        },
        {
            "id" : 003,
            "nama" : "Cintami Kartika",
            "nis" : "20.1.3",
            "alamat" : "Tajur",
            "hoby" : "Membaca"
        },
        {
            "id" : 004,
            "nama" : "Davha K. S",
            "nis" : "20.1.4",
            "alamat" : "Cisarua",
            "hoby" : "Olahraga"
        },
        {
            "id" : 005,
            "nama" : "Dede Inzaghi",
            "nis" : "20.1.5",
            "alamat" : "Gadog",
            "hoby" : "Game"
        }
    ]
}    
```

</td>
</tr>
</table>

### Update Siswa
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/siswa </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> PUT </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "id" : 001,
    "nama" : "Ahdi Kal Fatur",
    "nis" : "20.1.1",
    "alamat" : "Ciberem",
    "hoby" : "Musik"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Siswa Berhasil diubah",
    "data" : {
        "id" : 001,
        "nama" : "Ahdi Kal Fatur",
        "nis" : "20.1.1",
        "alamat" : "Ciberem",
        "hoby" : "Musik"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Alamat Siswa Telah digunakan",
    "data" : {
        "value" : "Ciberem",
        "property" : "alamat",
        "location" : "body"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Siswa tidak ditemukan",
    "data" : {
        "value" : 001,
        "property" : "id",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>

### Delete Siswa
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/siswa </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/siswa?id=001 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> DELETE </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=001 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses dihapus",
    "data" : {
        "id" : 001,
        "nama" : "Ahdi Kal Fatur",
        "nis" : "20.1.1",
        "alamat" : "Ciberem",
        "hoby" : "Musik"
    }
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Siswa tidak ditemukan",
    "data" : {
        "value" : 001,
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>
</details>

## Data Guru XI RPL
<details>
<summary> Klik untuk Ekspan </summary>

### Create Guru
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/guru </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> POST </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "nama" : "Muhamad Fikri, MOS",
    "nip" : "0010201",
    "alamat" : "Gadog",
    "mapel" : "Basisdata, Desain Grapis",
    "kelas" : "XI RPL, XI MM"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Guru Berhasil diinput",
    "data" : {
        "id" : "gr001",
        "nama" : "Muhamad Fikri, MOS",
        "nip" : "0010201",
        "alamat" : "Gadog",
        "mapel" : "Basisdata, Desain Grapis",
        "kelas" : "XI RPL, XI MM"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Guru Telah digunakan",
    "data" : {
        "value" : "Muhamad Fikri, MOS",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>


### Read Guru By Id
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/guru </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/guru?id=gr001 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=gr001 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "id" : "gr001",
        "nama" : "Muhamad Fikri, MOS",
        "nip" : "0010201",
        "alamat" : "Gadog",
        "mapel" : "Basisdata, Desain Grapis",
        "kelas" : "XI RPL, XI MM"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Guru tidak ditemukan",
    "data" : {
        "value" : "gr001",
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>


### Read Guru All
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/guru </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : 
        {
            "id" : "gr001",
            "nama" : "Muhamad Fikri, MOS",
            "nip" : "0010201",
            "alamat" : "Gadog",
            "mapel" : "Basisdata, Desain Grapis",
            "kelas" : "XI RPL, XI MM"
        },
        {
            "id" : "gr002",
            "nama" : "Selvia Prihastyani, S.Kom., Gr",
            "nip" : "0010202",
            "alamat" : "Ciapus",
            "mapel" : "Pemodelan Perangkat Lunak , Dasar-dasar Pengembangan Perangkat Lunak & Gim",
            "kelas" : "X RPL, XI RPL"
        },
        {
            "id" : "gr003",
            "nama" : "Muhamad Faisal Ramdani",
            "nip" : "0010203",
            "alamat" : "Megamendung",
            "mapel" : "Pemrograman Web dan Perangkat Bergerak  , Produk Kreatif dan Kewirausahaan",
            "kelas" : "XI RPL, XII RPL"
        }
    
}    
```

</td>
</tr>
</table>

### Update Guru
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/guru </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> PUT </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "id" : "gr003",
    "nama" : "Muhamad Faisal Ramdani, A.Md",
    "nip" : "0010203",
    "alamat" : "Megamendung",
    "mapel" : "Pemrograman Web dan Perangkat Bergerak  , Produk Kreatif dan Kewirausahaan",
    "kelas" : "XI RPL, XII RPL"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Guru Berhasil diubah",
    "data" : {
        "id" : "gr003",
        "nama" : "Muhamad Faisal Ramdani, A.Md",
        "nip" : "0010203",
        "alamat" : "Megamendung",
        "mapel" : "Pemrograman Web dan Perangkat Bergerak  , Produk Kreatif dan Kewirausahaan",
        "kelas" : "XI RPL, XII RPL"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Guru Telah digunakan",
    "data" : {
        "value" : "Muhamad Faisal Ramdani, A.Md",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Guru tidak ditemukan",
    "data" : {
        "value" : "gr003",
        "property" : "id",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>

### Delete Guru
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/guru </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/guru?id=gr001 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> DELETE </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=gr001 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses dihapus",
    "data" : {
        "id" : "gr001",
        "nama" : "Muhamad Fikri, MOS",
        "nip" : "0010201",
        "alamat" : "Gadog",
        "mapel" : "Basisdata, Desain Grapis",
        "kelas" : "XI RPL, XI MM"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Guru tidak ditemukan",
    "data" : {
        "value" : "gr001",
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>
</details>

## Data Mapel XI RPL
<details>
<summary> Klik untuk Ekspan </summary>

### Create Mapel
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mapel </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> POST </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "nama" : "Basisdata",
    "kode" : "BD",
    "kelas" : "XI RPL"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Mapel Berhasil diinput",
    "data" : {
        "id" : "mapel001",
        "nama" : "Basisdata",
        "kode" : "BD",
        "kelas" : "XI RPL"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Mapel Telah digunakan",
    "data" : {
        "value" : "Basisdata",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>


### Read Mapel By Id
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mapel</td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/mapel?id=mapel001 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=mapel001 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "id" : "mapel001",
        "nama" : "Basisdata",
        "kode" : "BD",
        "kelas" : "XI RPL"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Mapel tidak ditemukan",
    "data" : {
        "value" : "mapel001",
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>


### Read Mapel All
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mapel </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : 
        {
            "id" : "mapel001",
            "nama" : "Basisdata",
            "nip" : "BD",
            "kelas" : "XI RPL"
        },
        {
            "id" : "mapel002",
            "nama" : "Pemodelan Perangkat Lunak",
            "kode" : "PPL", 
            "kelas" : "XI RPL"
        },
        {
            "id" : "mapel003",
            "nama" : "Pemrograman Web dan Perangkat Bergerak",
            "kode" : "PWPB", 
            "kelas" : "XI RPL"
        }
    
}    
```

</td>
</tr>
</table>

### Update Mapel
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mapel </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> PUT </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "id" : "mapel001",
    "nama" : "Basis Data",
    "nip" : "BD",
    "kelas" : "XI RPL"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Mapel Berhasil diubah",
    "data" : {
        "id" : "mapel001",
        "nama" : "Basis Data",
        "nip" : "BD",
        "kelas" : "XI RPL"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Nama Mapel Telah digunakan",
    "data" : {
        "value" : "Basis Data",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Mapel tidak ditemukan",
    "data" : {
        "value" : "mapel001",
        "property" : "id",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>

### Delete Mapel
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/mapel </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/mapel?id=mapel001 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> DELETE </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=mapel001 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses dihapus",
    "data" : {
        "id" : "mapel001",
        "nama" : "Basis Data",
        "nip" : "BD",
        "kelas" : "XI RPL"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Mepel tidak ditemukan",
    "data" : {
        "value" : "mapel001",
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>
</details>

## Data Jadwal XI RPL
<details>
<summary> Klik untuk Ekspan </summary>

### Create Jadwal
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/jadwal </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> POST </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "hari" : "Senin",
    "guru" : "Muhamad Fikri, MOS",
    "mapel" : "Basisdata",
    "waktu" : "70 menit"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Jadwal Berhasil diinput",
    "data" : {
        "id" : "hr001",
        "hari" : "Senin",
        "guru" : "Muhamad Fikri, MOS",
        "mapel" : "Basisdata",
        "waktu" : "70 menit"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Jadwal Telah digunakan",
    "data" : {
        "value" : "Senin",
        "property" : "nama",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>


### Read Jadwal By Id
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/Jadwal</td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/Jadwal?id=hr001 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=hr001 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : {
        "id" : "hr001",
        "hari" : "Senin",
        "guru" : "Muhamad Fikri, MOS",
        "mapel" : "Basisdata",
        "waktu" : "70 menit"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Jadwal tidak ditemukan",
    "data" : {
        "value" : "hr001",
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>


### Read Jadwal All
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/jadwal </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> GET </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses",
    "data" : 
        {
            "id" : "hr001",
            "hari" : "Senin",
            "guru" : "Muhamad Fikri, MOS",
            "mapel" : "Basisdata",
            "waktu" : "70 menit"
        },
        {
            "id" : "hr002",
            "hari" : "Rabu",
            "guru" : "Selvia Prihastyani, S.Kom., Gr",
            "mapel" : "Pemodelan Perangkat Lunak",
            "waktu" : "105 menit"
        },
        {
            "id" : "hr003",
            "hari" : "Kamis",
            "guru" : "Muhamad Faisal Ramdani, A.Md",
            "mapel" : "Pemrograman Web dan Perangkat Bergerak",
            "waktu" : "70 menit"
        }
    
}    
```

</td>
</tr>
</table>

### Update Jadwal
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/jadwal </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> PUT </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Body</b> </td>
<td>

``` json
{
    "id" : "hr001",
    "hari" : "Senin",
    "guru" : "Muhamad Fikri, MOS",
    "mapel" : "Basisdata",
    "waktu" : "105 menit"
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 201,
    "message" : "Data Jadwal Berhasil diubah",
    "data" : {
        "id" : "hr001",
        "hari" : "Senin",
        "guru" : "Muhamad Fikri, MOS",
        "mapel" : "Basisdata",
        "waktu" : "105 menit"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Conflict</b> </td>
<td>

``` json
{
    "code" : 409,
    "message" : "Waktu Jadwal Telah digunakan",
    "data" : {
        "value" : "105 menit",
        "property" : "waktu",
        "location" : "body"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID jadwal tidak ditemukan",
    "data" : {
        "value" : "hr001",
        "property" : "id",
        "location" : "body"
    } 
}    
```

</td>
</tr>
</table>

### Delete Jadwal
<table>
<tr>
    <td> <b>URL</b> </td>
    <td> {{baseURL}}/api/v1/jadwal </td>
</tr>
<tr>
    <td> <b>Example</b> </td>
    <td> {{baseURL}}/api/v1/jadwal?id=jadwal001 </td>
</tr>
<tr>
    <td> <b>Method</b> </td>
    <td> DELETE </td>
</tr>
<tr>
    <td> <b>Header</b> </td>
    <td> Authorization : Bearer Token  </td>
</tr>
<tr>
<td> <b>Query</b> </td>
<td> id=jadwal001 </td>
</tr>
<tr>
<td> <b>Respon Success</b> </td>
<td>

``` json
{
    "code" : 200,
    "message" : "Sukses dihapus",
    "data" : {
        "id" : "hr001",
        "hari" : "Senin",
        "guru" : "Muhamad Fikri, MOS",
        "mapel" : "Basisdata",
        "waktu" : "105 menit"
    } 
}    
```

</td>
</tr>
<tr>
<td> <b>Respon Not Found</b> </td>
<td>

``` json
{
    "code" : 404,
    "message" : "ID Jadwal tidak ditemukan",
    "data" : {
        "value" : "hr001",
        "property" : "id",
        "location" : "query"
    } 
}    
```

</td>
</tr>
</table>
</details>