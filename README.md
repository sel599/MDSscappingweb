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
    
   <img width="426" alt="image" src="https://github.com/user-attachments/assets/0b3ff0ce-eef6-4935-a4de-e34148eae4b2" />


Tools yang digunakan pada project ini antara lain Phyton, RStudio, MongoDB dan Github.

# Document (MonggoDB)
   Berikut adalah salah satu contoh dokument di mongoDB :

    [{"$group": {"_id": "$Corporate Secretary","jumlah_emiten": { "$sum": 1 }}},{"$sort": { "jumlah_emiten": -1 }}]

# Analysis Agregasi Data Scrapping (Rstudio)
 Berikut merupakan link RPubs data scraping analysis : 
 
 (https://rpubs.com/Jefitarestii/projectmdskel6)
 
# PPT :
Berikut adalah link powerpoint berkaitan dengan project yang telah dibuat :
(https://www.canva.com/design/DAGo5dKJYeo/0pj9_cryemOhCLp6YJLXuA/edit?utm_content=DAGo5dKJYeo&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)

# Anggota :
  Project UAS MDS Kelompok 6
  
  <img width="341" alt="image" src="https://github.com/user-attachments/assets/eac2890a-b281-4816-ab67-e6c05ebd90af" />


 
