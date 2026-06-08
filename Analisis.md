Masalah pada Docker Compose (docker-compose.yml)<br>
Gejala: Container gagal build dan beberapa service tidak bisa saling terhubung.Penyebab:web1 menggunakan DB_HOST: mysql,sedangkan nama container database adalah mysql-db.web2 <br>
salah memasukkan password database (wrongpassword).web3 <br>
salah mengarahkan folder context ke ./web33 (seharusnya ./web3) dan tidak masuk ke dalam network frontend.Volume di bagian bawah bernama database-data, sedangkan di service db memanggil db-data.<br>
