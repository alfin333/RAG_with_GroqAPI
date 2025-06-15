<h1 align="center"> Retrieval-Augmented Generation with Gradio and Groq API Key</h1>
<p align="center"> Natural Language Processing Project</p>

<div align="center">

<img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">

</div>

### Name : Muhammad Alfin
### Tech Stack : Python, Gradio, LangChain, HuggingFace Embedding, FAISS vector store

---

### 1. Analysis about how the project works
- TODO

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
### 3. Analysis about how temperature works

```python
def get_llm():
    return ChatGroq(
        groq_api_key=GROQ_API_KEY,
        model_name="llama-3.3-70b-versatile",
        temperature=0.2 # Change the temperature value here and analzye
    )
```

3.1 Analysis on higher temperature 
- TODO

3.2 Analysis on lower temperature
- TODO

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

- TODO
- TODO
- TODO
- TODO
- TODO
- TODO
- TODO
