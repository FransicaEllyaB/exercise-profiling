# Tutorial Pemrograman Lanjut
## Fransisca Ellya Bunaren - 2306152286

## REFLECTION
1. What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?<br>

* <b>JMeter</b> digunakan untuk mengukur kinerja aplikasi dengan menyimulasikan banyak pengguna, contoh 10 0rang pada waktu bersamaan. Langkah ini untuk membantu mengidentifikasi bottleneck pada tingkat sistem, sperti respons server, throughput, dan kestabilan di bawah beban tinggi.
* <b>Intellij Profiler</b> digunakan untuk menganalisis performa internal aplikasi dengan fokus pada penggunaan CPU, memori, dan pemanggilan fungsi. Ini membantu developer menemukan kode tidak efisien dan mengoptimalkan penggunaan sumber daya. 

2. How does the profiling process help you in identifying and understanding the weak points in your application?<br>
Profiling membantu mengetahui titik lemah dalam aplikasi.
* Analisis Penggunaan CPU dengan menunjukkan fungsi atau proses mana yang paling banyak menggunakan CPU sehingga bisa dioptimalkan jika terjadi penggunaan berlebihan. 
* Pemantauan Memori dengan mengidentifikasi kebocoran memori (memory leaks) atau alokasi objek yang berlebihan yang dapat memperlambat aplikasi. 
* Deteksi Bottleneck Kode dengan menyoroti bagian kode yang paling lama dieksekusi, membantu mengoptimalkan algoritma atau logika bisnis yang lambat. 
* Analisis Thread dengan memeriksa deadlock, contention, atau inefisiensi dalam penggunaan thread yang bisa menyebabkan aplikasi tidak responsif. 
* Pemantauan Input/Output (I/O) dengan mengidentifikasi operasi I/O yang lambat, seperti akses database atau file yang dapat menjadi penyebab keterlambatan.

3. Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?
<br>IntelliJ Profiler sangat efektif dalam menganalisis dan mengidentifikasi bottleneck. Dengan integrasi langsung ke dalam IntelliJ IDEA, alat ini memungkinkan pemantauan performa secara real-time tanpa memerlukan perangkat tambahan. IntelliJ Profiler dapat mendeteksi metode yang lambat, penggunaan CPU yang berlebihan, serta kebocoran memori. Fitur seperti Flame Graph dan Call Tree Analysis memberikan visualisasi mendalam mengenai eksekusi metode dan hierarki pemanggilan fungsi, sementara CPU dan Memory Profiling membantu dalam mengidentifikasi algoritma yang tidak efisien serta masalah garbage collection. Selain itu, analisis thread memungkinkan deteksi dini terhadap isu konkurensi dan potensi deadlock. IntelliJ Profiler sangat berguna ketika aplikasi berjalan lambat tanpa alasan yang jelas, saat ada dugaan kebocoran memori, atau ketika ingin mengoptimalkan kode yang bersifat performa-kritis.


4. What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?<br>
* Memahami hasil profiling: Untuk menemukan bottlenecks, saya perlu memahami hasil profiling.
* Mengoptimisasi kode: Peforma aplikasi dapat dipengaruhi oleh kualitas kode dengan adanya refactoring peforma dapat menjadi lebih baik.

5. What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?
<br>IntelliJ Profiler membantu menganalisis performa kode aplikasi dengan integrasi langsung ke dalam IntelliJ IDEA sehingga tidak memerlukan alat tambahan. Dengan fitur pemantauan CPU dan memori secara real-time, saya dapat dengan mudah mendeteksi bottleneck, penggunaan sumber daya yang berlebihan, serta kebocoran memori.


6. How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?
<br>Untuk menghandle ketika terjadi inkonsisten Intellij Profiler dan Jmeter, saya akan memeriksa konfigurasi dengan memastikan bahwa lingkungan yang digunakan untuk kedua pengujian serupa. Lalu, saya akan melakukan pengujian ulang untuk memperoleh data yang lebih konsisten. 


7. What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?
<br>Strategi yang saya gunakan untuk optimasi kode adalah mengidentifikasi dan memfokuskan upaya pada bagian kode yang paling membebani sistem. Selain itu, mengurangi alokasi objek berlebihan dan menggunakan struktur data yang lebih efisien serta mengurangi waktu respons.

## Test Plan for Endpoints
<details>
<summary> /all-student-name</summary>
<b>Before Profiling and Performance Optimization</b>

* <b>View Results Tree</b>
  ![Screenshot 2025-03-13 081030](https://github.com/user-attachments/assets/42c50ad7-0a91-4192-8b7a-b503355545f6)


* <b>View Results in Table</b>
  ![Screenshot 2025-03-13 081043](https://github.com/user-attachments/assets/7b86c19c-66ec-49e4-832d-3739264342dc)

* <b>Summary Report</b>
  ![Screenshot 2025-03-13 081053](https://github.com/user-attachments/assets/8b5561fa-ae78-421b-a28a-20dbbb98f8e3)

* <b>Graph Results</b>
  ![Screenshot 2025-03-13 081105](https://github.com/user-attachments/assets/0999220d-fa2a-496c-8c6d-2f0f8f5edd20)

* Test Result JMeter
  ![Screenshot 2025-03-13 081214](https://github.com/user-attachments/assets/94dbc9f4-6da1-44d3-8f04-4c5796510881)

<b>After Profiling and Performance Optimization</b>

* <b>View Results Tree</b>
  ![Screenshot 2025-03-13 081715](https://github.com/user-attachments/assets/ce8ab15b-c47b-46b2-886a-a0547563ef3c)

* <b>View Results in Table</b>
  ![Screenshot 2025-03-13 081724](https://github.com/user-attachments/assets/bf1f5766-f243-4621-842f-e2d9653b0466)

* <b>Summary Report</b>
  ![Screenshot 2025-03-13 081734](https://github.com/user-attachments/assets/7a37f6d0-71bd-4085-8653-e9780c68b828)

* <b>Graph Results</b>
  ![Screenshot 2025-03-13 081741](https://github.com/user-attachments/assets/e3d395ba-02d7-4bb4-ad1b-8865839c3524)

* Test Result JMeter
  ![Screenshot 2025-03-13 081846](https://github.com/user-attachments/assets/a34f663f-8e37-47b1-a940-41a26a6950bc)

</details>

<details>
<summary> /highest-gpa</summary>
<b>Before Profiling and Performance Optimization</b>

* <b>View Results Tree</b>
  ![Screenshot 2025-03-13 081310](https://github.com/user-attachments/assets/669b2904-a781-485b-adfa-294ccfb905f8)

* <b>View Results in Table</b>
  ![Screenshot 2025-03-13 081324](https://github.com/user-attachments/assets/e570afe5-28d0-4129-b4b3-4909f1a191d8)

* <b>Summary Report</b>
  ![Screenshot 2025-03-13 081337](https://github.com/user-attachments/assets/fefdb95a-e895-423e-a809-d12ff7a9841c)

* <b>Graph Results</b>
  ![Screenshot 2025-03-13 081349](https://github.com/user-attachments/assets/dae28e47-43a3-464d-9d5f-67dfc03e6744)

* Test Result JMeter
  ![Screenshot 2025-03-13 081418](https://github.com/user-attachments/assets/aac10a04-f1f1-410d-a145-66ebe7f76a24)

<b>After Profiling and Performance Optimization</b>

* <b>View Results Tree</b>
  ![Screenshot 2025-03-13 081922](https://github.com/user-attachments/assets/eb90d008-7a0d-4a49-8a60-d7b63e13276e)

* <b>View Results in Table</b>
  ![Screenshot 2025-03-13 081930](https://github.com/user-attachments/assets/1a2ea0f0-efde-40c4-b887-a03097671486)

* <b>Summary Report</b>
  ![Screenshot 2025-03-13 081937](https://github.com/user-attachments/assets/68ca66a1-19bf-440a-b516-dd3594baeb15)

* <b>Graph Results</b>
  ![Screenshot 2025-03-13 081948](https://github.com/user-attachments/assets/76f29b96-0cc0-43ab-af06-7dcf18801fb2)

* Test Result JMeter
  ![Screenshot 2025-03-13 082024](https://github.com/user-attachments/assets/2c3cfad7-2b9e-4494-999d-a57ba83e041f)

</details>
