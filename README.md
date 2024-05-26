# Core Node Warden-buenavista'daki "OTO faucet isteme" kısmının editlenmiş halidir.

1) ilk önce ``` apt install screen ``` ile screen yoksa screen indirirn
```
screen -S restart
```
2) 
```
nano restart.sh
```
3) Açılan yere alttakini yapıştır
```
#!/bin/bash

# Sonsuz döngü başlat
while true; do
  # Komutunuzu burada çalıştırın
  sudo systemctl restart initiad
  
  # Echo ile mesajı yazdırın
  echo "restart atıldı"

  # 3 saat (10800 saniye) bekleyin
  sleep 10800
done
```

- ctr+x sonrasında y ve enter
4) 
```
chmod +x restart.sh
```
5) Çalıştırıyoruz
```
./restart.sh
```
- sonrasında pek elleşmeden ctrl a + d ile screen'den çıkıyoruz. (tekrar girmek istersek ``` screen -r restart ```)
