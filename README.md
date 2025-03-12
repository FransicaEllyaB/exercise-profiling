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
  ![Screenshot 2025-03-13 055443.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20055443.png)

* <b>View Results in Table</b>
  ![Screenshot 2025-03-13 055452.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20055452.png)

* <b>Summary Report</b>
  ![Screenshot 2025-03-13 055504.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20055504.png)

* <b>Graph Results</b>
  ![Screenshot 2025-03-13 055515.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20055515.png)

* Test Result JMeter
  ![Screenshot 2025-03-13 055745.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20055745.png)

<b>After Profiling and Performance Optimization</b>

* <b>View Results Tree</b>
  ![Screenshot 2025-03-13 003112.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20003112.png)

* <b>View Results in Table</b>
  ![Screenshot 2025-03-13 003122.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20003122.png)

* <b>Summary Report</b>
  ![Screenshot 2025-03-13 003135.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20003135.png)

* <b>Graph Results</b>
  ![Screenshot 2025-03-13 003146.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20003146.png)

* Test Result JMeter
  ![Screenshot 2025-03-13 003806.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20003806.png)

</details>

<details>
<summary> /highest-gpa</summary>
<b>Before Profiling and Performance Optimization</b>

* <b>View Results Tree</b>
  ![Screenshot 2025-03-13 055858.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20055858.png)

* <b>View Results in Table</b>
  ![Screenshot 2025-03-13 055911.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20055911.png)

* <b>Summary Report</b>
  ![Screenshot 2025-03-13 055925.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20055925.png)

* <b>Graph Results</b>
  ![Screenshot 2025-03-13 055936.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20055936.png)

* Test Result JMeter
  ![Screenshot 2025-03-13 060035.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20060035.png)

<b>After Profiling and Performance Optimization</b>

* <b>View Results Tree</b>
  ![Screenshot 2025-03-13 002730.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20002730.png)

* <b>View Results in Table</b>
  ![Screenshot 2025-03-13 002740.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20002740.png)

* <b>Summary Report</b>
  ![Screenshot 2025-03-13 002748.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20002748.png)

* <b>Graph Results</b>
  ![Screenshot 2025-03-13 002756.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20002756.png)

* Test Result JMeter
  ![Screenshot 2025-03-13 003232.png](..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2F..%2FPictures%2FScreenshots%2FScreenshot%202025-03-13%20003232.png)
</details>