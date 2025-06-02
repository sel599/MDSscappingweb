# Deskripsi Perusahaan BEI
<img width="662" alt="image" src="https://github.com/user-attachments/assets/6d2dba60-d30c-4c49-b5fd-1e408470b986" />

















Bursa Efek Indonesia (BEI) adalah lembaga yang menyelenggarakan dan menyediakan sistem serta sarana untuk memperdagangkan efek (seperti saham dan obligasi) di Indonesia. BEI berperan sebagai pasar tempat pertemuan antara perusahaan yang ingin menghimpun dana dari masyarakat (emiten) dan investor yang ingin menanamkan modal.
Fungsi utama BEI: *Menyediakan tempat perdagangan efek yang teratur, wajar, dan efisien.*Memfasilitasi perusahaan untuk melakukan penawaran umum (IPO). *Menyebarkan informasi pasar kepada publik dan pelaku pasar. *BEI berada di bawah pengawasan Otoritas Jasa Keuangan (OJK) dan merupakan hasil penggabungan Bursa Efek Jakarta (BEJ) dan Bursa Efek Surabaya (BES) pada tahun 2007.

# Project Scraping Data 
Tugas ini melakukan scraping data pada website : https://idx.co.id, dengan dua tujuan website yaitu 
1. Mengambil kode perusahaan tercatat apabila ada Perusahaan IPO baru yang melantai di Bursa Eefek Indonesia.
   Tujuan websie :  'https://idx.co.id/perusahaan-tercatat/




   <img width="691" alt="image" src="https://github.com/user-attachments/assets/aa71d20b-b0dc-4a4f-babb-1daac645016d" />














 
   Hasil Scarping pertama :

   <img width="317" alt="image" src="https://github.com/user-attachments/assets/79b0846e-0c70-437d-8040-0819d9a1ad84" />          


   Data :
   disimpan dalam .csv, Export Raw Format Dataframe to CSV dengan nama : ListPerusahaanIDX-22052025.csv
    df_listticker.to_csv('report/ListPerusahaanIDX-22052025.csv', sep='|', index=False) 
   
 2. Dari list poin 1, dilakukan scraping kembali untuk mengambil detail lengkap tentang profil informasi perusahaan seperti nama direksi, alamat hingga corporate secretary.
   Tujuan Website :  https://www.idx.co.id/id/perusahaan-tercatat/profil-perusahaan-tercatat/
   
     <img width="884" alt="image" src="https://github.com/user-attachments/assets/db55b4b2-fb49-4b13-a60e-59192a81d609" />













    Hasil Scraping kedua :

    
       <img width="727" alt="image" src="https://github.com/user-attachments/assets/e92a26f4-8419-4124-9431-f3645f7868e8" />
   
   
   
   
   
         Data : disimpan dalam .csv, Export Raw Format Dataframe to CSV dengan nama : BEI_Other_Data_Final-22052025.csv


# Data Final ( Phyton)
    
| Kolom                  | Type                   | Description                     		         |
|:---------------------------|:-----------------------|:-------------------------------------------------|
| Nama                   | TEXT			| Nama lengkap perusahaan (biasanya sesuai Akta Pendirian atau yang tercatat di IDX) |                      		             
| NPWP                 | INTEGER			  | Nomor Pokok Wajib Pajak perusahaan                   		             |
| Komite Audit Ketua                | TEXT		  | Nama ketua komite audit perusahaan                     	             |	
| Komite Audit Anggota 2-5                       | TEXT | Nama anggota komite audit lainnya, jika ada lebih dari satu anggota |                		                
| Direktur Utama                       | TEXT | Nama direktur utama/pimpinan tertinggi dalam struktur direksi |                                    
| Direktur 1,2,..dst	    	         | TEXT  | Nama direktur lain di jajaran direksi, bisa sampai Direktur n                |
| Komisaris	    	     | TEXT                | Tahun terbit novel                               |
| Corporate Secretary	    	             | TEXT| Nama pejabat yang bertanggung jawab atas keterbukaan informasi perusahaan |
| Established Date	    	 | DATE                | Tanggal resmi pendirian perusahaan sesuai Akta                            |
| Listing Date    	             | DATE                   | Tanggal pencatatan saham pertama kali di Bursa Efek Indonesia                        |
| Alamat	    	     | TEXT                  | Alamat lengkap kantor pusat perusahaan                                     |
| Phone		     | INTEGER			| Nomor telepon kantor perusahaan |
| Fax			     | INTEGER			| Nomor faksimile kantor (jika masih digunakan) |
| Homepage			     | TEXT			| URL situs web resmi perusahaan |
| Email			     | TEXT			 | Alamat email resmi perusahaan untuk korespondensi|
| Pemilik Saham 1			     | TEXT			 | Nama pemegang saham utama (umumnya pemegang saham pengendali atau pemilik mayoritas) |








Tools yang digunakan pada project ini antara lain Phyton, RStudio, MongoDB dan Github.

# Document (MonggoDB)
   Berikut adalah salah satu contoh dokument di mongoDB :

    [{"$group": {"_id": "$Corporate Secretary","jumlah_emiten": { "$sum": 1 }}},{"$sort": { "jumlah_emiten": -1 }}]

# Analysis Agregasi Data Scrapping (Rstudio)
 Berikut merupakan link RPubs data scraping analysis : 
 
 (https://rpubs.com/Jefitarestii/projectmdskel6)
 
# PPT :
Berikut adalah link powerpoint berkaitan dengan project yang telah dibuat :

(https://www.canva.com/design/DAGpKfSc5Iw/vh3koIHuI8ztIT-gArfk_A/edit?utm_content=DAGpKfSc5Iw&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

# Anggota :
  Project UAS MDS Kelompok 6
  
  | No | Nama                                    | NIM          |
|----|-----------------------------------------|--------------|
| 1  | Jefita Resti Sari                       | M0501241031  |
| 2  | Sely Fitriatun W                        | M0501241038  |
| 3  | Claudian Tikulimbong Tangdilomban       | M0501241048  |
| 4  | Baiq Nina Febriati                      | M0501241063  |


 
