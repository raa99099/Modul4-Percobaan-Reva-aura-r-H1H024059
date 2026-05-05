📘 Modul 4 - ADC & PWM (Kontrol Servo dengan Potensiometer)

👤 Identitas
Nama: Reva Aura Ramadhani
NIM: H1H024059
Mata Kuliah: Praktikum Sistem Mikrokontroler
Laboratorium: Multimedia Informatika UNSOED
📖 Deskripsi

Proyek ini mengimplementasikan Analog to Digital Converter (ADC) dan Pulse Width Modulation (PWM) pada Arduino untuk mengontrol servo motor menggunakan potensiometer.

💡 Sistem bekerja dengan cara:

Membaca nilai analog dari potensiometer (ADC)
Mengubahnya menjadi sudut (0°–180°)
Menggerakkan servo sesuai input (PWM)
🎯 Tujuan
 Memahami ADC dan PWM
 
Cara Kerja

Potensiometer menghasilkan tegangan analog (0–5V)
Arduino membaca nilai menggunakan analogRead()
Nilai dikonversi menggunakan fungsi map()
Servo digerakkan dengan myservo.write()

Penjelasan Modul

Pada Modul 4 ini dipelajari konsep Analog to Digital Converter (ADC) dan Pulse Width Modulation (PWM) pada Arduino. ADC digunakan untuk membaca sinyal analog dari potensiometer yang berupa tegangan (0–5V) dan mengubahnya menjadi nilai digital (0–1023). Nilai tersebut kemudian diproses oleh Arduino untuk digunakan dalam pengendalian output.

Selanjutnya, PWM digunakan untuk menghasilkan sinyal analog semu dengan cara mengatur lebar pulsa pada sinyal digital. Pada praktikum ini, nilai ADC dari potensiometer dikonversi menggunakan fungsi map() menjadi sudut servo (0°–180°). Servo kemudian bergerak sesuai nilai tersebut, sehingga posisi servo dapat dikontrol secara real-time berdasarkan input analog.

Dengan demikian, modul ini menunjukkan hubungan antara input analog dan output yang dikendalikan secara digital, serta bagaimana mikrokontroler dapat menjembatani keduanya dalam sebuah sistem kontrol sederhana.

Jawaban Pertanyaan

1. Bagaimana proses kerja sistem dari potensiometer hingga servo bergerak?
Proses dimulai dari potensiometer yang menghasilkan tegangan analog. Tegangan ini dibaca oleh Arduino melalui ADC menggunakan fungsi analogRead(), kemudian dikonversi menjadi nilai digital (0–1023). Nilai tersebut dipetakan menjadi sudut servo (0–180°) menggunakan fungsi map(), lalu dikirim ke servo menggunakan myservo.write(), sehingga servo bergerak sesuai posisi yang diinginkan.

2. Mengapa digunakan fungsi map() dalam program?
Fungsi map() digunakan untuk mengubah rentang nilai ADC (0–1023) menjadi rentang yang sesuai dengan kebutuhan servo (0–180°). Tanpa fungsi ini, nilai ADC tidak dapat langsung digunakan untuk mengontrol sudut servo secara tepat.

3. Apa yang terjadi jika nilai ADC kecil atau besar?
Jika nilai ADC kecil (mendekati 0), maka sudut servo juga kecil (mendekati 0°). Sebaliknya, jika nilai ADC besar (mendekati 1023), maka sudut servo mendekati 180°. Hal ini menunjukkan hubungan linier antara input dan output.

4. Apa fungsi delay(15) dalam program?
Fungsi delay(15) digunakan untuk memberikan waktu bagi servo agar bergerak secara stabil menuju posisi yang ditentukan. Tanpa delay, pergerakan servo bisa menjadi tidak stabil atau terlalu cepat berubah.
