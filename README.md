# LAB-42-RouterOS-Tools
Minggu 24 Agustus 2025  
  
# RouterOS Tools
  Sebelumnya kita sudah bahas Monitoring tools pada Mikrotik, sekarang kiya bahas RouterOS tools.  RouterOS tools ini ada banyak sekali, salah satunya tool-tool di monitoring yang sebelumnya kita bahas. Sekarang kita akan lanjutkan.  
    
# Packet Sniffer
  Untuk menangkap paket data yang lewat pada Interface. Analisis trafik paket untuk troubleshooting atau keamanan.  
  Contoh penggunaan:   

      tool sniffer start interface=ether1
  Untuk melihat hasilnya kita bisa mengunakan  

      tool sniffer packet print
# Schenduler
  Menjalankan perintah secara otomatis berdasarkan waktu tertentu. Otomatisasi tugas rutin, saperti reboot harian. Contoh penggunaan.  

      system scheduler add interval=1d on-event="/system reboot" name=autoReboot

# E-mail tool
  Untuk mengirim notifikasi atau laporan ke alamat email administrator, mendukung sistem  monitoring berbasis alert. Contoh penggunaan:  

      tool e-mail send ahnaf@gmail.com subject="Router Status" body="OK"

# SMS Tool 
  Mengirim dan menerima SMS melalui router, alternatif notifikasi jika internet bermasalah.  Router harus pakai modem GSM. Contoh penggunaan.  

      tool sms send phone-number=+628xxx message="Router Down"
# SNTP Client
  Sinkronisasi waktu router dengan server NTP, menjaga waktu router teteap akurat.  
  Contoh penggunaan:  

      system ntp client set enabled=yes primary-ntp=203.89.146.1
# Flood ping
  Mengirim ping dalam jumlah besar, menguji ketahanan jaringan dan mendeteksi packet loss.   
  Contoh penggunaan:  

      ping 8.8.8.8 count=1000
# IP Scan
  Memindai perangkat yang aktif dalam suatu segmen jaringan, mengetahui IP adddress yang digunakan di jaringan.  
  Contoh penggunaan:  

      tool ip-scan 192.168.1.0/24


# Kesimpulan 
  MikroTik Tools adalah seperangkat fasilitas bawaan RouterOS yang mendukung administrator dalam memantau, menguji, dan mengelola jaringan. Mulai dari alat dasar seperti ping hingga fasilitas kompleks seperti packet sniffer dan scheduler, semua memiliki peran penting dalam mendukung manajemen jaringan yang efisien.

# Sumber
https://help.mikrotik.com/docs/spaces/ROS/pages/8323205/IP+Scan  
https://citraweb.com/artikel_lihat.php?id=55  
