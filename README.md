*Penjelasan Modul*

Pada Modul 4 ini dipelajari konsep Analog to Digital Converter (ADC) dan Pulse Width Modulation (PWM) pada sistem mikrokontroler Arduino. ADC berfungsi untuk mengubah sinyal analog yang berasal dari potensiometer menjadi data digital dengan rentang nilai 0 hingga 1023. Nilai ini merepresentasikan tegangan input dari 0V hingga 5V.

Selanjutnya, data digital tersebut digunakan untuk mengontrol perangkat output melalui PWM. PWM merupakan teknik untuk menghasilkan sinyal analog semu dengan mengatur lebar pulsa (duty cycle) pada sinyal digital. Dalam praktikum ini, nilai ADC dikonversi menjadi sudut servo (0°–180°) menggunakan fungsi map().

Servo motor kemudian digerakkan sesuai dengan nilai hasil konversi tersebut menggunakan fungsi myservo.write(). Dengan demikian, posisi servo dapat dikendalikan secara real-time berdasarkan perubahan nilai potensiometer.

Modul ini menunjukkan bagaimana mikrokontroler dapat menghubungkan input analog dengan output yang dikontrol secara digital, sehingga dapat digunakan dalam berbagai aplikasi sistem kontrol seperti robotika dan otomasi.

Jawaban Pertanyaan

1. Jelaskan alur kerja sistem pada percobaan ini!
Proses dimulai dari potensiometer yang menghasilkan tegangan analog. Tegangan tersebut dibaca oleh Arduino melalui pin analog menggunakan fungsi analogRead(), kemudian dikonversi menjadi nilai digital (0–1023). Nilai ini dipetakan menjadi sudut servo (0–180°) menggunakan fungsi map(). Selanjutnya, Arduino mengirimkan sinyal PWM ke servo menggunakan myservo.write() sehingga servo bergerak sesuai nilai input.

2. Mengapa digunakan fungsi analogRead()?
Fungsi analogRead() digunakan untuk membaca nilai tegangan analog dari potensiometer. Karena Arduino bekerja dengan data digital, maka sinyal analog perlu dikonversi terlebih dahulu menjadi nilai digital agar dapat diproses oleh mikrokontroler.

3. Apa fungsi dari map() dalam program?
Fungsi map() digunakan untuk mengubah rentang nilai ADC (0–1023) menjadi rentang sudut servo (0–180°). Hal ini diperlukan agar nilai yang dibaca dari potensiometer dapat sesuai dengan kebutuhan pengendalian servo.

4. Apa yang terjadi jika nilai ADC meningkat?
Jika nilai ADC meningkat, maka nilai sudut servo juga meningkat. Akibatnya, servo akan berputar ke posisi yang lebih besar. Hal ini menunjukkan hubungan linier antara input analog dan output servo.

5. Apa fungsi dari PWM pada percobaan ini?
PWM digunakan untuk mengontrol posisi servo dengan mengatur sinyal pulsa yang dikirimkan. Meskipun servo tidak menggunakan PWM biasa seperti LED, prinsip dasar PWM tetap digunakan dalam pengaturan posisi melalui sinyal kontrol.

6. Apa fungsi dari myservo.write()?
Fungsi myservo.write() digunakan untuk mengatur sudut putaran servo sesuai dengan nilai yang diberikan (0°–180°).

7. Mengapa diperlukan delay(15) dalam program?
Delay digunakan untuk memberikan waktu bagi servo agar dapat mencapai posisi yang diinginkan secara stabil. Tanpa delay, perubahan nilai yang terlalu cepat dapat menyebabkan gerakan servo menjadi tidak halus.

8. Apa yang terjadi jika potensiometer tidak terhubung dengan benar?
Jika potensiometer tidak terhubung dengan benar, nilai ADC yang terbaca bisa tidak stabil atau selalu bernilai tetap (0 atau 1023), sehingga servo tidak bergerak sesuai yang diharapkan.

9. Bagaimana hubungan antara ADC dan PWM dalam sistem ini?
ADC digunakan untuk membaca input analog, sedangkan PWM digunakan untuk mengontrol output (servo). Keduanya bekerja bersama untuk menghubungkan input analog dengan output yang dikendalikan secara digital.
