# Module 5: Java Profiling

### /all-student-name

- **Graph Results**
  ![Graph Results](images/Graph%20result_1.png)
- **View Results Table**
  ![View Results Table](images/Result%20table_1.png)
- **Summary Report**
  ![Summary Report](images/Summary%20report_1.png)
- **View Result Tree**
  ![View Result Tree](images/Result%20tree_1.png)

### /highest-gpa

- **Graph Results**
  ![Graph Results](images/Graph%20result_2.png)
- **View Results Table**
  ![View Results Table](images/Result%20table_2.png)
- **Summary Report**
  ![Summary Report](images/Summary%20report_2.png)
- **View Result Tree**
  ![View Result Tree](images/Result%20tree_2.png)

### Test result /all-student-name
```
timeStamp,elapsed,label,responseCode,responseMessage,threadName,dataType,success,failureMessage,bytes,sentBytes,grpThreads,allThreads,URL,Latency,IdleTime,Connect
1741947109117,216,highest-gpa request,500,,Thread Group 2 1-1,text,false,,256,127,3,3,http://localhost:8080/highest-gpa,211,0,16
1741947109247,123,highest-gpa request,500,,Thread Group 2 1-3,text,false,,256,127,3,3,http://localhost:8080/highest-gpa,123,0,0
1741947109147,231,highest-gpa request,500,,Thread Group 2 1-2,text,false,,256,127,2,2,http://localhost:8080/highest-gpa,231,0,0
1741947109346,35,highest-gpa request,500,,Thread Group 2 1-4,text,false,,256,127,1,1,http://localhost:8080/highest-gpa,35,0,1
1741947109446,8,highest-gpa request,500,,Thread Group 2 1-5,text,false,,256,127,1,1,http://localhost:8080/highest-gpa,8,0,0
1741947109546,7,highest-gpa request,500,,Thread Group 2 1-6,text,false,,256,127,1,1,http://localhost:8080/highest-gpa,7,0,1
1741947109646,11,highest-gpa request,500,,Thread Group 2 1-7,text,false,,256,127,1,1,http://localhost:8080/highest-gpa,11,0,1
1741947109746,7,highest-gpa request,500,,Thread Group 2 1-8,text,false,,256,127,1,1,http://localhost:8080/highest-gpa,6,0,1
1741947109846,13,highest-gpa request,500,,Thread Group 2 1-9,text,false,,256,127,1,1,http://localhost:8080/highest-gpa,13,0,1
1741947109944,10,highest-gpa request,500,,Thread Group 2 1-10,text,false,,256,127,1,1,http://localhost:8080/highest-gpa,10,0,1

```

### Test result /highest-gpa
```
timeStamp,elapsed,label,responseCode,responseMessage,threadName,dataType,success,failureMessage,bytes,sentBytes,grpThreads,allThreads,URL,Latency,IdleTime,Connect
1741947276960,32,all-student-name request,500,,Thread Group 3 1-1,text,false,,261,132,1,1,http://localhost:8080/all-student-name,29,0,18
1741947277002,56,all-student-name request,500,,Thread Group 3 1-2,text,false,,261,132,1,1,http://localhost:8080/all-student-name,56,0,1
1741947277101,13,all-student-name request,500,,Thread Group 3 1-3,text,false,,261,132,1,1,http://localhost:8080/all-student-name,12,0,1
1741947277202,11,all-student-name request,500,,Thread Group 3 1-4,text,false,,261,132,1,1,http://localhost:8080/all-student-name,11,0,0
1741947277302,12,all-student-name request,500,,Thread Group 3 1-5,text,false,,261,132,1,1,http://localhost:8080/all-student-name,12,0,1
1741947277400,15,all-student-name request,500,,Thread Group 3 1-6,text,false,,261,132,1,1,http://localhost:8080/all-student-name,15,0,1
1741947277501,7,all-student-name request,500,,Thread Group 3 1-7,text,false,,261,132,1,1,http://localhost:8080/all-student-name,7,0,1
1741947277601,11,all-student-name request,500,,Thread Group 3 1-8,text,false,,261,132,1,1,http://localhost:8080/all-student-name,11,0,1
1741947277701,13,all-student-name request,500,,Thread Group 3 1-9,text,false,,261,132,1,1,http://localhost:8080/all-student-name,12,0,1
1741947277801,13,all-student-name request,500,,Thread Group 3 1-10,text,false,,261,132,1,1,http://localhost:8080/all-student-name,13,0,1

```

## Refleksi

> What is the difference between the approach of performance testing with JMeter and profiling with IntelliJ Profiler in the context of optimizing application performance?

JMeter digunakan untuk menguji performa sistem dengan mensimulasikan banyak pengguna sekaligus, mengukur kecepatan respons dan kapasitasnya. Sementara itu, IntelliJ Profiler menganalisis cara kerja kode secara mendalam untuk menemukan masalah seperti penggunaan CPU dan memori yang tidak efisien. JMeter membantu mengevaluasi kinerja aplikasi dalam skenario nyata, sedangkan Profiler berfokus pada mengidentifikasi dan memperbaiki inefisiensi dalam kode.

> How does the profiling process help you in identifying and understanding the weak points in your application?

Profiling membantu menemukan kelemahan dalam aplikasi dengan memberikan gambaran mendalam tentang cara kode dijalankan. Dengan profiling, kita bisa melihat metode mana yang paling banyak menggunakan CPU, bagaimana memori dialokasikan, dan apakah ada kebocoran memori yang membuat aplikasi boros sumber daya. Selain itu, profiling juga dapat mengidentifikasi thread yang berjalan lambat atau mengalami deadlock, sehingga masalah akibat konkurensi bisa dideteksi lebih awal. Data dari profiler membantu pengembang fokus pada bagian kode yang benar-benar menyebabkan performa menurun, sehingga optimasi bisa dilakukan dengan lebih tepat dan efisien.

> Do you think IntelliJ Profiler is effective in assisting you to analyze and identify bottlenecks in your application code?

IntelliJ Profiler adalah alat yang efektif untuk menganalisis dan menemukan bagian kode yang memperlambat aplikasi. Dengan berbagai fitur visualisasi seperti Call Tree, Flame Graph, dan Memory Profiling, pengembang bisa dengan mudah melihat penggunaan CPU dan memori. Selain itu, alat ini membantu mengukur berbagai aspek performa aplikasi secara real-time, sehingga masalah bisa ditemukan dan diperbaiki lebih cepat.

> What are the main challenges you face when conducting performance testing and profiling, and how do you overcome these challenges?

Beberapa tantangan utama adalah membuat skenario pengujian yang sesuai, memahami data profiling yang kompleks, dan memastikan perbaikan tidak menimbulkan masalah baru. Saya mengatasinya dengan menggunakan alat uji otomatis, mencatat setiap perubahan dengan jelas, dan melakukan pengujian berkala untuk menjaga kestabilan aplikasi.

> What are the main benefits you gain from using IntelliJ Profiler for profiling your application code?

IntelliJ Profiler membantu menemukan masalah performa dalam kode dengan cepat. Alat ini bisa menunjukkan bagian kode yang paling banyak menggunakan sumber daya, mengecek penggunaan memori, dan mendeteksi kebocoran yang bisa membuat aplikasi lambat atau crash. Dengan fitur Live Profiling, pengguna bisa langsung melihat bagaimana perubahan kode memengaruhi aplikasi. Secara keseluruhan, alat ini membuat kode lebih efisien dan mengurangi penggunaan sumber daya yang tidak perlu.

> How do you handle situations where the results from profiling with IntelliJ Profiler are not entirely consistent with findings from performance testing using JMeter?

Jika hasil dari JMeter dan Profiler tidak sesuai, langkah pertama yang saya lakukan adalah memeriksa kembali skenario pengujian dan memastikan lingkungan uji memiliki konfigurasi yang sama. Saya juga menjalankan tes tambahan untuk membandingkan hasil dan mencari faktor yang mungkin memengaruhi perbedaan tersebut, seperti data uji atau pengaturan sistem.

> What strategies do you implement in optimizing application code after analyzing results from performance testing and profiling? How do you ensure the changes you make do not affect the application's functionality?

Saya mengutamakan optimasi berdasarkan seberapa besar dampaknya terhadap kinerja. Langkah-langkah yang saya ambil termasuk memperbaiki algoritma, mengurangi penggunaan memori, dan memperbaiki struktur kode. Untuk memastikan perubahan tidak merusak fungsi aplikasi, saya melakukan pengujian ]dan integrasi secara menyeluruh, serta menerapkan integrasi berkelanjutan untuk memvalidasi perilaku aplikasi setelah setiap optimasi.