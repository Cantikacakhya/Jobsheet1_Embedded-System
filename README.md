# Jobsheet1_Embedded-System
Dasar Pemrograman Esp32 Untuk Pemrosesan Data Input/Output Analog Dan Digital

I.PENJELASAN SINGKAT

Praktikum ini menggunakan ESP32 yang merupakan mikrokontroler yang dikenalkan oleh Espressif System yang merupakan penerus dari mikrokontroler ESP8266. Dalam ESP32 tersedia modul WiFi dalam chip dan bluetooth sehingga sangat mendukung untuk membuat sistem aplikasi Internet of Things. Pin analog pada ESP32 memiliki fitur yang dapat mengubah sinyal analog yang masuk menjadi nilai digital yang mudah diukur. Pin analog terhubung dengan converter pada mikrokontroller yang dikenal dengan istilah analog-to-digital converter (disingkat ADC atau A/D). Analog output pada microkontroller dihasilkan oleh teknik yang dikenal dengan istilah PWM atau Pulse Width Modulation. PWM memanipulasi keluaran digital sedemikian rupa sehingga menghasilkan sinyal analog. Metode PWM menggunakan pendekatan perubahan lebar pulsa untuk menghasilkan nilai tegangan analog yang diinginkan. Sedangkan regresi analisis adalah teknik statistika untuk menginvestigasi dan memodelkan hubungan antara variabel dari data statistik sebelumnya. Praktikum ini bertujuan supaya dapat memahami dan melakukan pengolahan data untuk input/output analog dan digital dan melakukan optimalisasi pembacaan sensor analog menggunakan metode regresi linear.

II. ALAT DAN BAHAN 

    1) ESP32 
    2) Breadboard 
    3) Kabel jumper 
    4) Potensiometer 10k Ohm (1)
    5) Sensor Capacitive Soil Moisture 
    6) LED (5) dan Push Button (3)
    7) Multimeter 
    8) Resistor 330,1K, 10K Ohm (@ 3)

III. LANGKAH PERCOBAAN 

      A.Instalasi Board ESP32 pada Arduino IDE 
        1. Buka Arduino IDE 
        2. Klik Menu File > Preferences
        3. Pada kolom Additional ... yang ada dibawah, tambahkan link berikut https://dl.espressif.com/dl/package_esp32_index.json 
        4. Klik menu Tools > Board: > Pilih Boards Manager ...
        5. Pada kolom pencarian tulis ESP32 kemudian install dan tunggu hingga selesai
        
      B.Mengakses GPIO dan PWM ESP32
        a) GPIO
          1. Buatlah rangkaian seperti pada gambar di bawah ini (Gambar 1)    
![1](https://user-images.githubusercontent.com/121161133/209552320-5606302a-75c8-4d8e-9bf6-211c79cf5dfc.png)
     
          2. Buka program example blink, kemudian modifikasi dan buat agar LED dapat melakukan blink dengan interval 100ms, 1 detik, 2 detik dan 3 detik sekali. LED dapat blink 1 detik sekali menggunakan timer milis().
          3. Buatlah program seperti pada script GPIO1.ino untuk mengendalikan led menggunakan push button. Kemudian upload program tersebut pada ESP32 dan hasilnya akan seperti video di bawah ini (GPIO1)


https://user-images.githubusercontent.com/121161133/209610801-54b11bdf-779d-4f9f-bee8-debfc7d0863a.mp4


          4. Tambahkan 1 LED dan 1 push button pada rangkaian, kemudian kembangkan program agar ketika push button ke-2 ditekan, LED akan melakukan blink setiap 500 ms sekali. Hasilnya akan seperti pada video di bawah ini (GPIO2)


https://user-images.githubusercontent.com/121161133/209611151-8210b0dc-6839-483d-9c3b-4aef98e46f28.mp4


          5. Tambahkan 3 LED dan 1 push button pada rangkaian, kemudian kembangkan program agar ketuka push button ke-3 ditekan, LED akan menyala menjadi running led (menyala bergantian dari kiri ke kanan). Hasilnya akan seperti pada video di bawah ini (GPIO3)


https://user-images.githubusercontent.com/121161133/209611182-05d617ce-8862-4005-a33e-180caf2d49d3.mp4


        b) PWM 
           1. Buatlah rangkaian seperti pada gambar berikut (gambar 2)
![2](https://user-images.githubusercontent.com/121161133/209552694-acdca979-9e74-4d8a-a38f-4d32bc8b586d.png)

           2. Buatlah script program seperti pada script GPIO2.ino.
           3. upload program dan hasilnya akan seperti pada video di bawah ini (PWM1)


https://user-images.githubusercontent.com/121161133/209611220-937211b9-ea75-47a5-8364-a5f909a7ac7d.mp4


           4. Buatlah program lanjutan seperti pada script GPIO3.ino
           5. upload program dan hasilnya akan seperti pada video di bawah ini (PWM2)
 

https://user-images.githubusercontent.com/121161133/209611238-0053e1bd-3ae0-4cc5-b669-dacdfe271792.mp4



       C.ADC dan DAC 
         1. Buatlah rangkaian seperti pada gambar di bawah ini (gambar 3)
![3](https://user-images.githubusercontent.com/121161133/209552883-4ae204c2-588f-4ed7-bec1-c92816e58ef3.png)

         2. Buatlah program seperti pada script ADC-DAC1.ino
         3. Putar potensiometer secara perlahan agar mendapatkan nilai 0 hingga 4095 pada tampilan serial monitor. Hasilnya akan seperti video di bawah ini (ADC-DAC1)


https://user-images.githubusercontent.com/121161133/209611275-e5543afd-9a08-4391-9fcd-c1b4ae695254.mp4


         4. Buatlah program seperti pada script ADC-DAC2.ino.Tambahkan LED pada GPIO 5.
         5. Upload program, kemudian putar potensiometer dari nilai terendah hingga nilai tertinggi. Hasilnya akan seperti pada video di bawah ini (ADC-DAC2)


https://user-images.githubusercontent.com/121161133/209612667-f1f70676-dd37-4076-b51f-2aa920d1f92d.mp4






