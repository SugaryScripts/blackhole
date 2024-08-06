PEMANFAATAN OPENAI SEBAGAI CUSTOMER SERVICE UNTUK MENJAWAB FAQ PERUSAHAAN / ORGANISASI MELALUI PLATFORM WHATSAPP
Batasan:
- Temp Token for WhatsApp
- Free Plan Render.com (no disk)
- Chat Bot & Embedding function are from OpenAI
- Dokumen PDF secara tekstual
Tech:
- Flask - python
- Postgre as DB
- Framework Langchain 
- FAISS as a vectorstore
#### PERANCANGAN SISTEM

#### HASIL DAN PEMBAHASAN
- Sistem Percakapan
- Sistem ChatBot
- Webservice
- Deploy
- WhatsApp WebHook

##### Sistem Percakapan 
Pengembangan percakapan dalam penelitian ini dimulai dengan membuat fungsi untuk mengolah dokumen PDF menjadi vectorstore. Fungsi embedding yang digunakan untuk mengubah dokumen menjadi vectorstore adalah dengan OpenAIEmbeddings(). Di mana fungsi embedding itu juga berasal dari OpenAI. 
-- kode load pdf splitter sampai generate faiss
Pada kode di atas, yang mempengaruhi kualitas hasil dan kuantitas token yang digunakan adalah salah satunya pada fungsi splitter. Di mana, pada penelitian ini akan di tetapkan jumlah potongan sebanyak 1000 karakter dan *overlap* sebanyak 200 karakter.
Untuk meminimalisasi penggunaan token OpenAI, diperlukan juga untuk menyimpan vectorstore secara lokal. Agar pada aplikasi tidak akfif di server, vectorstore yang telah dibuat tidak terhapus. Di mana hal tersebut bisa teratasi dengan menambahkan fungsi berikut.
Kode save dan load vectorstore
Setiap kali percakapan dimulai, aplikasi akan memanggil fungsi pada kode di atas untuk mencari pengetahuan yang relevan dengan percakapan. Serta apabila aplikasi mendeteksi perubahan pada dokumen, aplikasi hanya tinggal memanggil fungsi simpan setiap pembuatan vectorstore selesai.

##### percakapan
