# Cara Build wxWidgets di Windows

## Pendahuluan

wxWidgets adalah library c++ open source yang berguna untuk membuat aplikasi berbasis GUI dengan tampilan yang native.

Native artinya, tampilan wxWidgets serupa dengan GUI yang ada di sistem operasi.

Library ini bersifat gratis dan open source.

## Cara Mem-Build wxWidgets dengan Visual Studio Community 2022

Mem-build wxWidgets dari source code penting untuk dilakukan, terutama untuk memastikan bahwa file library (.lib di Visual Studio c++) kompatibel dengan linker yang ada di Visual Studio sehingga tidak menimbulkan linker error.

Berikut ini saya bahas cara membuild wxWidgets 3.0.5 dengan Visual Studio Community 2022.

### 1. Mendownload Visual Studio Community 2022 dan Menginstallnya

Untuk mendownload Visual Studio Community 2022, silakan kunjungi:

- https://visualstudio.microsoft.com/vs/community/

Selanjutnya, jalankan installer dan install:

- Program utama dari Visual Studio

- Komponen "**Desktop Development with C++**". Biarkan pilihan default dari komponen ini.

### 2. Mendownload wxWidgets 3.0.5

Untuk mendownload wxWidgets 3.0.5, silakan kunjungi:

- https://github.com/wxWidgets/wxWidgets/releases/download/v3.0.5/wxWidgets-3.0.5.zip

### 3. Mengekstrak File Zip wxWidgets 3.0.5

Untuk mengekstraknya, pertama copy dahulu "**wxWidgets-3.0.5.zip**" ke folder yang Anda inginkan.

Selanjutnya Anda bisa mengekstraknya dengan 7zip.

Pastikan Anda mengekstraknya ke dalam folder terpisah agar tidak berantakan.

Kalau dengan 7zip dengan memilih "**Extract to wxWidgets-3.0.5**".

![ScreenShot](assets/gambar1.png?raw=true)

### 4. Mem-Build wxWidgets 3.0.5 dengan Visual Studio

Setelah diekstrak, buka "**Windows Explorer**" ke dalam folder "**wxWidgets-3.0.5**".

Masuk ke folder "**build/msw**" dan temukan file "**wx_vc12.sln**".

![ScreenShot](assets/gambar2.png?raw=true)

Buka file .sln tadi dengan "**Visual Studio Community 2022**".

Setelah dibuka, maka file tadi akan dikonversi ke versi yang sesuai. Jika ada tawaran "**Retarget Projects**" di sini, klik ok saja.

Selanjutnya, buka "**menu > Build > Batch Build**".

Nanti akan muncul dialog yang berisi daftar centang.

Di sini, klik "**Select Al**l".

Kemudian, klik "**Build**".

![ScreenShot](assets/gambar3.png?raw=true)

Proses build akan sedikit memakan waktu. Harap menunggu.

### 5. Mencoba Contoh Kode yang Disediakan wxWidgets 3.0.5

Sekarang proses build sudah selesai.

Akan ada banyak file .lib yang dihasilkan.

Lokasi file .lib berada di folder lib.

Lebih jelasnya:

- Library yang menggunakan .dll dan .lib ada di "**lib/vc_dll**"

- Library static ada di "**lib/vc_lib**"

- Library versi x64 dari kedua poin di atas ada di "**vc_x64_dll**" dan "**vc_x64_lib**"

Untuk mengetahui file .lib mana yang dibutuhkan project Anda, akan lebih baik jika Anda mengecek contoh kodenya.

Selanjutnya Anda tinggal melihat file .lib mana yang digunakan dalam project setting dari contoh kode tadi.

Untuk mencoba contoh kode, pertama tama "**Save All**" terlebih dahulu project saat ini, kemudian tutup Visual Studio Community 2022.

Selanjutnya, navigasi ke folder "**samples/aui**".

Buka file "**auidemo_vc9.vcproj**" dengan Visual Studio Community 2022.

Jika ada pesan "**One Way Upgrade**", klik OK.

Nanti project barusan akan dikonversi ke project Visual Studio Community 2022.

Saat baru dibuka "**Save All**" dan jika ada tawaran untuk membuat Solution, save dengan nama yang Anda inginkan.

Selanjutnya, buka "**menu > Debug > Start Without Debugging**".

Jika proses build lancar, maka akan tampil sebuah window GUI.

![ScreenShot](assets/gambar4.png?raw=true)