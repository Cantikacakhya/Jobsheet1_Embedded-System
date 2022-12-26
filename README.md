# Jobsheet1_Embedded-System
Dasar Pemrograman Esp32 Untuk Pemrosesan Data Input/Output Analog Dan Digital

I.PENJELASAN SINGKAT
    Praktikum ini menggunakan ESP32 yang merupakan mikrokontroler yang dikenalkan oleh Espressif System merupakan penerus dari mikrokontroler ESP8266. Tersedia modul WiFi dalam chip, bluetooth sehingga sangat mendukung untuk membuat sistem aplikasi Internet of Things. Pin analog pada ESP32 Hanya saja pin analog memiliki fitur untuk dapat mengubah sinyal analog yang masuk menjadi nilai digital yang mudah diukur. Pin analog terhubung dengan converter pada mikrokontroller yang dikenal dengan istilah analog-to-digital converter (disingkat ADC atau A/D). Analog output pada microkontroller dihasilkan oleh teknik yang dikenal dengan istilah PWM atau Pulse Width Modulation. PWM memanipulasi keluaran digital sedemikian rupa sehingga menghasilkan sinyal analog. Metode PWM menggunakan pendekatan perubahan lebar pulsa untuk menghasilkan nilai tegangan analog yang diinginkan. 
    Regresi analisis adalah teknik statistika untuk menginvestigasi dan memodelkan hubungan antara variabel dari data statistik sebelumnya.
Praktikum ini bertujuan supaya dapat memahami dan melakukan pengolahan data untuk input/output analog dan digital dan melakukan optimalisasi pembacaan sensor analog menggunakan metode regresi linear.

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
          1. Buatlah rangkaian seperti pada Gambar 1 
          2. Buka program example blink, kemudian modifikasi dan buat agar LED dapat melakukan blink dengan interval 100ms, 1 detik, 2 detik dan 3 detik sekali. 
             LED dapat blink 1 detik sekali menggunakan timer milis(). Dokumentasikan hasilnya. (video 1)
          3. Buatlah program seperti pada script GPIO1.ino untuk mengendalikan led menggunakan push button. Kemudian upload program tersebut pada ESP32 (hasilnya pada              video GPIO 1)
          4. Tambahkan 1 LED dan 1 push button pada rangkaian, kemudian kembangkan program agar ketika push button ke-2 ditekan, LED akan melakukan blink setiap 500 ms              sekali. (Hasilnya pada video GPIO 2)
          5. Tambahkan 3 LED dan 1 push button pada rangkaian, kemudian kembangkan program agar ketuka push button ke-3 ditekan, LED akan menyala menjadi running led                (menyala bergantian dari kiri ke kanan). (Hasilnya pada video GPIO 3).
        b) PWM 
           1. Buatlah rangkaian seperti pada gambar 2
           2. Buatlah script program seperti pada script GPIO2.ino.
           3. upload program dan hasilnya akan seperti pada video PWM1
           4. Buatlah program lanjutan seperti pada script GPIO3.ino
           5. upload program dan hasilnya akan seperti pada video PWM2

       C.ADC dan DAC 
         1. Buatlah rangkaian seperti pada gambar 3
         2. Buatlah program seperti pada script ADC-DAC1.ino
         3. Putar potensiometer secara perlahan agar mendapatkan nilai 0 hingga 4095 pada tampilan serial monitor. (hasilnya pada video ADC-DAC1)
         4. Buatlah program seperti pada script ADC-DAC2.ino.Tambahkan LED pada GPIO 5.
         5. Upload program, kemudian putar potensiometer dari nilai terendah hingga nilai tertinggi. (hasilnya pada video ADC-DAC2)



