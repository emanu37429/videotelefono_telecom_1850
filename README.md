# videotelefono_telecom_1850

Presumo sia quello indicato in questo topic: https://www.ilpuntotecnico.com/forum/index.php/topic,4934.0.html

L'ho comprato per sbaglio pensando fosse l'Hi-Tel (esteriormente appaiono uguali).

Per fare un backup di /usr:
1) Connetti un cavo Ethernet. Inserisci una SD formattata in FAT16 o FAT32 (dimensione massima 1GB)
2) Premi Menù, dopodiché Zoom (sopra il 3), Video off (sotto la cornetta rossa), di nuovo Zoom
3) Nel menù di test che si apre, scorri le voci fino a S/W download, premi OK, poi vai su Enable INETD poi di nuovo OK
4) Connettiti al telefono via telnet (user "root")
5) Dai questi comandi:

```
cd /tmp
mkdir mntmmc
mount /dev/mmc/disc0/part1 /tmp/mntmmc
tar -cvpzf /tmp/mntmmc/usr_back.tar /usr
