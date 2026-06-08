Masalah pada Docker Compose (docker-compose.yml)<br>
Gejala: Container gagal build dan beberapa service tidak bisa saling terhubung.<br>
Penyebab:
-web1 menggunakan DB_HOST: mysql,sedangkan nama container database adalah mysql-db.<br>
-web2 salah memasukkan password database (wrongpassword).<br>
-web3 salah mengarahkan folder context ke ./web33 (seharusnya ./web3) dan tidak masuk ke dalam network frontend.<br>
-Volume di bagian bawah bernama database-data, sedangkan di service db memanggil db-data.<br>
