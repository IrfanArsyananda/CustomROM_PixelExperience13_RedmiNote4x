# Memasang _Custom ROM_ PixelExperience di Redmi Note 4X
Syarat : **Perangkat MIUI sudah UBL (Unlock Bootloader)**

1. Mengunduh semua bahan
   - Minimal ADB Fastboot (<a href="https://androiddatahost.com/uq6us">Unduh</a>) | (<a href="https://sfile.mobi/1qxDzlsaw0O7">Alternatif Unduh</a>) | (<a href="https://androidmtk.com/download-minimal-adb-and-fastboot-tool">Sumber</a>) | (<a href="https://androidmtk.com/install-minimal-adb-and-fastboot-tool">Cara Pasang</a>)
   - 15 Seconds ADB Installer (<a href="https://androiddatahost.com/jzkh5">Unduh</a>) | (<a href="https://androidmtk.com/download-15-seconds-adb-installer">Sumber</a>) | (<a href="https://androidmtk.com/download-best-android-adb-driver">Cara Pasang</a>)
   - OrangeFox Recovery (<a href="https://sourceforge.net/projects/nranjan-17/files/RETROFIT%20OrangeFox/OrangeFox-R11.1-A12-RETROFIT-Unofficial-mido.zip/download">Unduh</a>) | (<a href="https://www.mediafire.com/file/wxz60ewkhv1nx1j/OrangeFox-mido-stable@R11.1_2_A12_dynamic.zip/file">Alternatif Unduh</a>) | (<a href="https://get.pixelexperience.org/mido">Sumber</a>) | (<a href="https://raw.githubusercontent.com/NRanjan-17/Pixel-Experience-Releases/main/RETROFIT_GUIDE.md">Cara Pasang</a>) / Buka Video Referensi 1
   - TWRP Recovery (<a href="https://sourceforge.net/projects/alone0316/files/recovery/twrp-3.7.0_12.0-mido-A13.img/download">Unduh</a>) | (<a href="https://raw.githubusercontent.com/NRanjan-17/Pixel-Experience-Releases/main/RETROFIT_GUIDE.md">Sumber</a>) | (<a href="https://raw.githubusercontent.com/NRanjan-17/Pixel-Experience-Releases/main/RETROFIT_GUIDE.md">Cara Pasang</a>) / Buka Video Referensi 1
   - PixelExperience 13 ROM (<a href="https://get.pixelexperience.org/mido">Unduh</a>) | (<a href="https://get.pixelexperience.org/mido">Sumber</a>) | (<a href="https://raw.githubusercontent.com/NRanjan-17/Pixel-Experience-Releases/main/RETROFIT_GUIDE.md">Cara Pasang</a>) / Buka Video Referensi 2
   - DM Verity (<a href="https://sfile.mobi/9FrnDrBbZSp">Unduh</a>) | Cara Pasang Buka Video Referensi 1
2. Langkah eksekusi
   - Pasang Minimal ADB Fastboot (Install biasa di PC)
   - Pasang 15 Seconds ADB Installer (Install biasa di PC)
   - Ekstrak file *OrangeFox.zip*, pindahkan file *recovery.img* dari OrangeFox ke dalam folder pemasangan Minimal ADB Fastboot (Default di **C:\Program Files (x86)\Minimal ADB and Fastboot**)
   - Sambungkan USB PC ke HP, aktifkan mode USB Debugging di menu opsi pengembang
   - Di dalam direktori **C:\Program Files (x86)\Minimal ADB and Fastboot** buka file *cmd-here.exe*
   - Memasang OrangeFox atau TWRP Recovery (Dalam posisi terminal terbuka)
        - (a) Cek perangkat : ```adb devices```  
         <span style="color:red">*Jika tertulis unauthorized, izinkan usb debugging dengan klik OK pada layar HP, lalu ulangi langkah **(a)**</span>
        - (b) Masuk ke mode bootloader : ```adb reboot bootloader```
        - (c) Cek perangkat dalam mode fastboot : ```fastboot devices```  
         <span style="color:red">*Jika perangkat otomatis restart sendiri, kemungkinan dapat diatasi dengan memasang/memperbarui driver (Cek folder **Fix Update Driver** pada repository ini) pada posisi perangkat mode fastboot</span>
        - (d) Flash recovery : ```fastboot flash recovery.img```  
        <span style="color:red">*Jika mengalami error pada salah satu langkah diatas, disarankan untuk mengulang lagi dari langkah **(a)** sampai **(d)**
   - Masuk ke mode recovery
        - (e) Pada keadaan perangkat mati, tekan dan tahan tombol power + volume atas secara bersamaan
        - (f) Format data perangkat via OrangeFox/TWRP (**jangan reboot dulu**)
        - (g) Pasang *DM Verity.zip* via OrangeFox/TWRP
        - (h) Reboot System
        - Masuk kembali ke mode recovery seperti langkah **(e)**  
        <span style="color:red">*Jika tidak bisa masuk atau mode recovery OrangeFox/TWRP tidak terbaca, ulangi pemasangan dari awal langkah **(a)**</span>
   - Memasang Custom ROM (Posisi Perangkat Mode Recovery OrangeFox/TWRP)
        - (i) Lakukan Wipe Dalvik, Cache, System, Data, Internal (**kecualikan internal jika file bahan ada disana**)
        - (j) Pasang Custom ROM via OrangeFox/TWRP (**jangan reboot dulu**)
        - (k) Format data via OrangeFox/TWRP
        - (l) Reboot ke sistem  
         <span style="color:red">*Jika gagal masuk ke menu OS atau bootloop, ulangi dari langkah **(i)**</span>

   
## Referensi Video
 1. <a href="https://www.youtube.com/watch?v=J_i_wNzJABY">Cara Pasang TWRP OrangeFox di Redmi Note 4X</a>
 2. <a href="https://www.youtube.com/watch?v=gKSu2bz4KY8">Tutorial Install ROM PixelExperience Redmi Note 4X</a>
