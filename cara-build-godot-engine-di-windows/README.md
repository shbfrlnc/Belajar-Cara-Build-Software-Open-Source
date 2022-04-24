# Cara Build Godot Engine di Windows

## Pendahuluan

Godot Engine adalah game engine open source yang dapat digunakan untuk membuat game 2D maupun 3D bagi berbagai platform.

Kali ini kita akan belajar cara mem-build Godot Engine dari source code nya di Windows 10.

Hal ini mungkin perlu dilakukan karena boleh jadi kita:

- Ingin berkontribusi dalam pengembangannya

- Mengembangkan modul Godot Engine

- Meng-extend Godot Engine

- Mem-fork Godot Engine versi kita sendiri

## Persiapan

### 1. Python 3.5+

Sebelum kita mulai, pastikan Python 3.5+ sudah terinstall di sistem operasi dan dapat dijalankan melalui command line di folder manapun.

Untuk mendownloadnya, kunjungi:

https://www.python.org/

Untuk itu, pastikan Python 3.5+ sudah ditambahkan ke PATH di environment variables.

Untuk menambahkan Python 3.5+ ke PATH di environment variables, silakan pelajari sendiri caranya.

### 2. Visual Studio Community 2022

Selain Python tadi, kita juga perlu menginstall Visual Studio Community.

Karena saya menggunakan yang 2022, maka saya menyarankan untuk menggunakan Visual Studio Community 2022.

Untuk mendownloadnya, silakan kunjungi:

https://visualstudio.microsoft.com/vs/community/

Setelah Visual Studio Community 2022 terdownload, jalankan installernya, kemudian pilih komponen "Desktop Development with C++" untuk diinstall:

![](assets/desktop-development-with-cpp.png?raw=true)

Setelah terinstall, kita lanjutkan.

### 3. SCons 3.0

Kita juga perlu menginstall SCons 3.0.

Caranya, buka command line, kemudian:

```
python -m pip install scons
```

### 4. Source Code Godot Engine

Untuk mendownload versi stable dari Godot Engine, kunjungi:

https://github.com/godotengine/godot/releases

Saya membahas yang versi 3.4.4-stable.

Jadi, sebaiknya samakan.

## Proses Build

Setelah semua persiapan siap, kita ekstrak source code Godot Engine di sebuah folder kosong.

Selanjutnya, buka folder source code Godot Engine.

Di folder tersebut, buka command line.

Selanjutnya jalankan:

```
scons platform=windows
```

Maka, proses build akan berjalan:

![](assets/compiling.png?raw=true)

Ini akan sedikit memakan waktu. Harap sabar.

Setelah selesai, buka folder "[GodotSourceCode]/bin".

Yang mana nama folder "[GodotSourceCode]" tergantung versi Godot Engine yang Anda download.

Kalau di saya: "godot-3.4.4-stable".

Di sana akan ada Binary dari Godot Engine.

## Penutup

Sekian cara build Godot Engine di Windows.

Selamat mencoba.




























