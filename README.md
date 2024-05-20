# Core Node Warden-buenavista'daki "OTO faucet isteme" kısmının editlenmiş halidir.

1) 
```shell

screen -S restart

```
2) 
```shell

nano restart.sh

```
3) Açılan yere alttakini yapıştır
```shell

#!/bin/bash

# Sonsuz döngü başlat
while true; do
  # Komutunuzu burada çalıştırın
  sudo systemctl restart initiad

  # 6 saat (21600 saniye) bekleyin
  sleep 21600
done

```

- ctr+x sonrasında y ve enter
4) 
```shell

chmod +x restart.sh

```
5) Çalıştırıyoruz
```shell

./restart.sh

```

- sonrasında pek elleşmeden ctrl a + d ile screen'den çıkıyoruz. (tekrar girmek istersek screen -r restart)
