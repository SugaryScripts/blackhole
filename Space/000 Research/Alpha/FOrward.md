##### Less
###### Latar Belakang
- Diperlukannya desain halaman dengan UI/UX yang menarik agar pengguna membaca FAQ [How many people really read the FAQs of any website? - Quora](https://www.quora.com/How-many-people-really-read-the-FAQs-of-any-website)
- Butuh waktu dan ketelitian dalam pencarian informasi dari FAQ
- Adanya realitas pelanggan malu untuk bertanya
- Penyediaan pelayanan pelanggan membutuhkan ekstra waktu dan biaya
- Pelanggan terkadang harus datang dan bertanya
###### Batasan masalah
- Menghiraukan media apapun dalam platform WA
- Menghiraukan dokumen dengan gambar
##### 3 Analisis dan perancangan sistem
###### Desain dan Perancangan sistem
- RAG
- Sistem Chatbot
###### Perancangan Pengujian
- 
##### 5
###### Saran
- Diperlukan untuk embedding gambar juga selain text
- Melakukan verifikasi bisnis WhatsApp agar dapat menggunakan token permanent dari official WhatsApp
- Instruksi penggunaan didetailkan pada saat pengumpulan survei data, agar mendapatkan feedback yang sesuai dengan aplikasi
##### Challenge naive RAG
- Bad retrieval
	- Low precision
	- low recall: lack enough context for LLM to synthesize the answer
	- Outdated info: data is redundant or out of date
- Bad response
	- Hallucination: Model makes up an answer that isn't in the context
	- Irrelevance: answer that doesn't answer the question
	- Toxicity/Bias: answer that harmful or offensive
##### RAG System
Doc -> Chunks -> vector database -> chunks -> LLM
Data -> embeddings -> retrieval -> synthesis

