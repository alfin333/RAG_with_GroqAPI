<h1 align="center"> Retrieval-Augmented Generation with Gradio and Groq API Key</h1>
<p align="center"> Natural Language Processing Project</p>

<div align="center">

<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">

</div>

### Name : Muhammad Alfin
### Tech Stack : Python, Gradio, LangChain, HuggingFace Embedding, FAISS vector store

---

### 1. Analysis about how the project works
- Proyek ini adalah aplikasi sederhana yang memungkinkan pengguna untuk mengunggah file PDF dan mengajukan pertanyaan berdasarkan isi dokumen tersebut menggunakan teknik Retrieval-Augmented Generation (RAG). Aplikasi ini menggunakan Groq API Key untuk mengakses LLM yang kuat sehingga mampu memberikan jawaban kontekstual berdasarkan dokumen yang diunggah. Dalam proyek ini, saya mengunggah file berjudul "Muhammad Alfin_CV" yang berisi curriculum vitae saya untuk direview dan dianalisis melalui aplikasi.

### 2. Analysis about how different every model works on Retrieval-Augmented Generation
###    Document RAG for analysis: CV of Muhammad Alfin 
```python
def get_llm():
    return ChatGroq(
        groq_api_key=GROQ_API_KEY,
        model_name="llama-3.3-70b-versatile", # Change the model in the code
        temperature=0.2
    )
```
- Model used : ```[llama-3.3-70b-versatile, deepseek-r1-distill-llama-70b, gemma2-9b-it]```

2.1 Analysis on ```llama-3.3-70b-versatile``` : 
- Prompt: apa saja keahlian yang dia miliki ?
- Answer:
```
Berdasarkan informasi yang tersedia, Muhammad Alfin memiliki keahlian sebagai berikut:
**Bahasa:**

* Indonesia (Penutur Asli)
* Inggris (Kemampuan Tingkat Menengah)

**Hard Skills:**

* HTML
* CSS
* Javascript
* PHP
* MySQL
* Python
* Laravel
* Flask
* Restful API
* Flutter

**Soft Skills:**

* Analitis
* Kerja Sama Tim
* Manajemen Waktu
* Komunikasi Efektif

Selain itu, dia juga memiliki pengalaman dalam pengembangan aplikasi, sistem pendataan, dan proyek-proyek lainnya yang terkait dengan teknologi dan pengembangan perangkat lunak.
```
Analysis:
```
1. Pemahaman Konteks: Model langsung menjawab pertanyaan berdasarkan informasi eksplisit/permukaan
2. Integrasi tambahan: Tidak melakukan inferensi tambahan seperti menyimpulkan dari pengalaman proyek atau menambahkan keahlian turunan
3. Struktur: Rapi, namun pasif (karena menampilkan informasi eksplisitnya saja)
```
2.2 Analysis on ```deepseek-r1-distill-llama-70b``` : 
- Prompt: apa saja keahlian yang dia miliki ?
- Answer:
```
<think>
Okay, so I need to figure out what skills Muhammad Alfin has based on the provided context. Let me go through each section step by step.

First, under the "Kemampuan & Kompetensi" section, it lists both hard and soft skills. The hard skills include HTML, CSS, JavaScript, PHP, MySQL, Python, Laravel, Flask, Restful API, and Flutter. Soft skills are analytical thinking, teamwork, time management, and effective communication.

Looking at his education, he's studying Software Engineering, which probably covers a lot of programming areas. His projects also give clues about his skills. For example, in the Infinite Learning project, he worked on AI algorithms like content-based filtering and the Traveling Salesman Problem, so that adds AI and machine learning to his skills.

In the Toko Sumber Rahayu project, he developed a POS application using Laravel and Flutter, which means he has experience with web and mobile development. He also worked on RESTful APIs and database design, so those are additional skills.

His experience with the UKM IMAM project involved building a web application with PHP, which reinforces his web development skills. Additionally, his involvement in the Robotika organization shows he can handle system design and data management with tools like Excel.

His organizational experience as a leader in OSIS SMP Angkasa Pura indicates strong leadership and organizational skills, which are soft skills.

So, compiling all this, his skills include programming languages, frameworks, AI, data management, leadership, and more. I should list all these points clearly to answer the question about his skills.
</think>

Muhammad Alfin memiliki berbagai keahlian yang mencakup keterampilan teknis dan non-teknis. Berikut adalah rincian keahliannya:

### Keahlian Teknis (Hard Skills):
1. **Bahasa Pemrograman**: HTML, CSS, JavaScript, PHP, MySQL, Python.
2. **Framework dan Library**: Laravel, Flask, Restful API, Flutter.
3. **Teknologi dan Algoritma**: 
   - Artificial Intelligence (AI)
   - Machine Learning
   - Algoritma seperti Content-Based Filtering dan Traveling Salesman Problem (TSP)
4. **Database dan API**: Desain database, pengembangan RESTful API.
5. **Pengembangan Aplikasi**: Web dan mobile development.

### Keahlian Non-Teknis (Soft Skills):
1. **Analitis**: Kemampuan analisis dan pemecahan masalah.
2. **Kerja Sama Tim**: Pengalaman dalam memimpin dan bekerja dalam tim.
3. **Manajemen Waktu**: Kemampuan mengatur waktu secara efektif.
4. **Komunikasi Efektif**: Kemampuan berkomunikasi dengan baik dalam tim dan dengan klien.
5. **Kepemimpinan**: Pengalaman memimpin proyek dan organisasi.

### Pengalaman Praktis:
- **Proyek Infinite Learning**: Mengembangkan aplikasi wisata dengan fitur rekomendasi dan perencanaan rute optimal.
- **Toko Sumber Rahayu**: Membangun aplikasi POS berbasis web dan mobile.
- **UKM IMAM**: Membuat aplikasi pemantauan keuangan berbasis web.
- **Robotika Politeknik Negeri Banyuwangi**: Merancang sistem pendataan komponen robotika untuk meningkatkan efisiensi.

Muhammad Alfin menunjukkan kemampuan yang kuat dalam pengembangan perangkat lunak, dengan fokus pada teknologi terbaru seperti Artificial Intelligence, serta kemampuan kepemimpinan dan kerja tim yang efektif. 
```
- Analysis:
```
1. Pemahaman Konteks: Sangat baik, model menyampaikan skill yang eksplisit dan menyimpulkan keahlian dari berbagai bagian (proyek, pengalaman organisasi).
2. Integrasi Informasi: Model melakukan reasoning antarkonten dan menyatukan insight dari beragam dokumen atau segmen teks.
3. Struktur: Komprehensif, bernarasi, dan mendalam. Menunjukan reasoning pada tag <think>. (Namun seharusnya tag ini tidak perlu ditampilkan sebagai output default)
```
2.3 Analysis on ```gemma2-9b-it``` : 
- Prompt: apa saja keahlian yang dia miliki ?
- Answer:
```
Based on the text provided, here are Muhammad Alfin's skills:

**Languages:**

* Indonesian (Native)
* English (Intermediate)

**Hard Skills:**

* HTML
* CSS
* Javascript
* PHP
* MySQL
* Python
* Laravel
* Flask
* Restful API
* Flutter

**Soft Skills:**

* Analytical
* Teamwork
* Time Management
* Effective Communication 


Let me know if you have any other questions.

```
- Analysis:
```
1. Pemahaman Konteks: Model langsung menjawab pertanyaan berdasarkan informasi eksplisit/permukaan (namun model ini lebih singkat dibanding llama-3.3-70b-versatile)
2. Integrasi tambahan: Tidak melakukan inferensi tambahan seperti menyimpulkan dari pengalaman proyek atau menambahkan keahlian turunan
3. Struktur: Rapi, namun pasif (karena menampilkan informasi eksplisitnya saja)
```
### 3. Analysis about how temperature works

```python
def get_llm():
    return ChatGroq(
        groq_api_key=GROQ_API_KEY,
        model_name="llama-3.3-70b-versatile",
        temperature=0.2 # Change the temperature value here and analzye
    )
```

3.1 Analysis on higher temperature (0.9)
Model: llama-3.3-70b-versatile
- Prompt: apa ada yang perlu diperbaiki dari cv dia ?
- Answer:
```
Berikut beberapa saran untuk perbaikan CV Muhammad Alfin:

1. **Format dan Tata Letak**: CV masih terlihat seperti teks yang dipangkas dari dokumen lain. Sebaiknya, gunakan format yang lebih rapi dan mudah dibaca, dengan menggunakan judul, subjudul, dan spasi yang tepat.
2. **Bahasa**: Beberapa kalimat masih menggunakan bahasa yang kurang formal atau tidak tepat. Pastikan bahasa yang digunakan profesional dan sesuai dengan konteks.
3. **Konsistensi**: Terdapat beberapa kesalahan ketik dan tidak konsisten dalam penggunaan tanda baca. Periksa kembali CV untuk memastikan tidak ada kesalahan.
4. **Pengalaman Kerja**: Pengalaman kerja yang disajikan masih terlalu singkat dan tidak memberikan gambaran yang jelas tentang tanggung jawab dan prestasi yang dicapai. Sebaiknya, tambahkan lebih banyak detail tentang proyek yang dikerjakan, peran yang dimainkan, dan hasil yang dicapai.
5. **Kemampuan dan Kompetensi**: Daftar kemampuan dan kompetensi yang disajikan masih terlalu panjang dan tidak terstruktur dengan baik. Sebaiknya, kelompokkan kemampuan dan kompetensi ke dalam kategori yang lebih spesifik dan relevan dengan posisi yang dilamar.
6. **Pendidikan**: Informasi pendidikan masih kurang lengkap. Sebaiknya, tambahkan informasi tentang jurusan, IPK, dan tahun lulus.
7. **Proyek**: Proyek yang disajikan masih terlalu singkat dan tidak memberikan gambaran yang jelas tentang proyek yang dikerjakan. Sebaiknya, tambahkan lebih banyak detail tentang proyek, peran yang dimainkan, dan hasil yang dicapai.
8. **Kata Kunci**: Sebaiknya, tambahkan kata kunci yang relevan dengan posisi yang dilamar untuk memudahkan recruiter menemukan CV.

Dengan perbaikan-perbaikan tersebut, CV Muhammad Alfin dapat menjadi lebih efektif dalam menyajikan informasi tentang kemampuan, pengalaman, dan prestasi yang dicapai.
```
- Analysis: Gaya bahasa lebih ekspresif dan naratif, model memberikan saran yang luas dan beragam, model berani menuangkan ide-ide luas seperti "tambahkan detail proyek" dan "kelompokkan kemampuan" menunjukkan eksplorasi yang luas, cocok untuk brainstorming (mengumpulkan gagasan, ide, solusi)

3.2 Analysis on lower temperature (0.1)
Model: llama-3.3-70b-versatile
- Prompt: apa ada yang perlu diperbaiki dari cv dia ?
- Answer:
```
Berikut beberapa saran untuk perbaikan CV Muhammad Alfin:

1. **Format dan Tata Letak**: CV terlihat seperti teks yang dipanjangkan tanpa format yang jelas. Saran: gunakan format yang lebih terstruktur, dengan judul, subjudul, dan paragraf yang jelas.
2. **Konsistensi Ejaan dan Tanda Baca**: Terdapat beberapa kesalahan ejaan dan tanda baca, seperti penggunaan spasi yang tidak konsisten. Saran: periksa kembali CV untuk memastikan ejaan dan tanda baca yang benar.
3. **Penggunaan Bahasa**: Bahasa yang digunakan terkadang tidak formal atau tidak sesuai dengan konteks CV. Saran: gunakan bahasa yang lebih formal dan profesional.
4. **Penjelasan yang Terlalu Panjang**: Beberapa penjelasan tentang proyek atau pengalaman kerja terlalu panjang dan tidak efektif. Saran: ringkas penjelasan menjadi poin-poin yang lebih singkat dan efektif.
5. **Kurangnya Spesifikasi**: Beberapa bagian CV, seperti "Kemampuan & Kompetensi", kurang spesifik dan tidak menjelaskan secara detail kemampuan yang dimiliki. Saran: tambahkan contoh atau penjelasan yang lebih spesifik tentang kemampuan yang dimiliki.
6. **Tidak Ada Foto**: CV tidak memiliki foto, yang dapat membantu memperkuat identitas dan profesionalisme. Saran: tambahkan foto yang profesional dan sesuai dengan konteks CV.
7. **Kurangnya Informasi tentang Prestasi**: CV tidak menyebutkan prestasi atau penghargaan yang telah diterima. Saran: tambahkan informasi tentang prestasi atau penghargaan yang relevan dengan bidang yang diminati.
8. **Perlu Lebih Banyak Kata Kunci**: CV tidak memiliki kata kunci yang cukup untuk membantu recruiter atau sistem pencarian CV menemukan CV tersebut. Saran: tambahkan kata kunci yang relevan dengan bidang yang diminati.

Dengan memperbaiki beberapa hal di atas, CV Muhammad Alfin dapat menjadi lebih efektif dan profesional.
```
- Analysis: Gaya bahasa ringkas dan terstruktur, model memberikan respon yang jelas, langsung, dan aman, model lebih formal dan preskriptif dalam memberikan jawaban, cocok untuk review cepat dan teknis

### 4. How to run the project

- Clone this repository with : 

```git
git clone https://github.com/arifian853/RAG_with_GroqAPI.git
```

- Copy the ```.env.example``` file and rename it to ```.env```

```
GROQ_API_KEY=your-groq-api-key
```

- Fill the ```GROQ_API_KEY``` with your Groq API Key, find it here : https://console.groq.com/keys

- Make virtual environment:
  ```
  python -m venv venv
  ```
- Activate the virtual environment:
  ```
  venv\Scripts\activate        # Windows
  source venv/bin/activate      # macOS/Linux
  ```
  Note: if error, try execute "Set-ExecutionPolicy RemoteSigned" on powershell as administrator, then try to activate the venv again
- Install dependencies:
  ```
  pip install -r requirements.txt
  ```
- Run the program:
  ```
  python app.py
  ```
- Open on browser URL: http://127.0.0.1:7860
- or Open on public URL: https://23d2474eefc32b07db.gradio.live
  Note: this code "demo.launch(share=True)" must be set True first, (it's on app.py)
