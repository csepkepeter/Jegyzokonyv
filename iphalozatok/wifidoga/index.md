# MÉRÉSI JEGYZŐKÖNYV
# Méréstechnikai Feladat: Hálózati topológia kiépítése és a megfelelő internet kapcsolat biztosítása    

**A mérést végző neve:** Csépke Péter  
**A mérés tárgya:**   Hálózati topológia kiépítése és a megfelelő internet kapcsolat biztosítása  
**A mérés száma:** órai mérés 01.  
**A mérés dátuma:** 2025.02.06.  
**A mérést vezette:** Csontos Dénes  

**Évfolyam:** 13. E  
**Csoport:** GYAK 1  
**Helyszín:** Fizikai  

### A mérés célja  
Hálózati topológia kiépítése és a megfelelő internet kapcsolat biztosítása.

### Méréshez használt eszközök  

1. CISCO Catalyst 1000 Series Switch  
2. Tenda W268R WiFi Router  
3. HP Laptop
4. Honor 50 okostelefon  
-----
## Topológia  
![topo](https://github.com/user-attachments/assets/ac47ad29-5e97-49e9-a94b-99df92e12c96)

-----
## WiFi router beállítása  
**Router ip címe**
![lan set](https://github.com/user-attachments/assets/f44970f7-bdbd-40b4-86ad-86bb8865d91f)

**DHCP beállítása**
![dhcp beall](https://github.com/user-attachments/assets/51fbe2da-9294-40d8-a000-01c620bf996e)

**SSID és biztonság**
![ssid](https://github.com/user-attachments/assets/ffd5441e-d998-4e9a-aad9-58b3bf023112)  
![wifi secu](https://github.com/user-attachments/assets/4dd8e72f-4d1d-4224-ab21-2e32e358c4b7)  

## Tesztek  
**IP cím lekérése**  
![ipconfig](https://github.com/user-attachments/assets/fa9d7a27-df86-42cf-888e-09b7f1e118fd)  
**IP eldobása**  
![ip eldobas](https://github.com/user-attachments/assets/b0135cf5-e53a-469d-aeec-3b1f8581cbe2)  
**Új ip cím kérés**  
![ip kérés](https://github.com/user-attachments/assets/1e7ef3b6-319b-4630-9569-ced478017940)

**Routing tábla**  
![port lista](https://github.com/user-attachments/assets/6fdc6b0b-e31c-4a46-93d5-d4d943b347a1)

**Microsoft.com teszt**   
![microsoft test](https://github.com/user-attachments/assets/41fcbc0a-1b53-4a2a-8bce-3ba426954f19)

**Ipon.hu nyomonkövetés**  
![ipon kovetes](https://github.com/user-attachments/assets/5c369ed0-144b-4485-91e1-a9d9ceb633c3)

**Használt portok listája**  
C:\Users\Tanulo>netstat -r

Interface List  
 22...0a 00 27 00 00 16 ......VirtualBox Host-Only Ethernet Adapter  
 12...72 66 55 62 61 d1 ......Microsoft Wi-Fi Direct Virtual Adapter #3  
 17...f2 66 55 62 61 d1 ......Microsoft Wi-Fi Direct Virtual Adapter #4  
 18...b0 5c da 21 f1 bf ......Realtek PCIe GbE Family Controller  
 11...70 66 55 62 61 d1 ......Realtek RTL8822CE 802.11ac PCIe Adapter  
  1...........................Software Loopback Interface 1  

**IPv4 Routing table**  

| Network Destination   | Netmask          | Gateway         | Interface       | Metric |
|-----------------------|------------------|-----------------|-----------------|--------|
| 0.0.0.0               | 0.0.0.0          | 192.168.6.254   | 192.168.6.195   | 35     |
| 127.0.0.0             | 255.0.0.0        | On-link         | 127.0.0.1       | 331    |
| 127.0.0.1             | 255.255.255.255   | On-link         | 127.0.0.1       | 331    |
| 127.255.255.255       | 255.255.255.255   | On-link         | 127.0.0.1       | 331    |
| 192.168.6.192         | 255.255.255.192   | On-link         | 192.168.6.195   | 291    |
| 192.168.6.195         | 255.255.255.255   | On-link         | 192.168.6.195   | 291    |
| 192.168.6.255         | 255.255.255.255   | On-link         | 192.168.6.195   | 291    |
| 192.168.56.0          | 255.255.255.0     | On-link         | 192.168.56.1    | 281    |
| 192.168.56.1          | 255.255.255.255   | On-link         | 192.168.56.1    | 281    |
| 192.168.56.255        | 255.255.255.255   | On-link         | 192.168.56.1    | 281    |
| 224.0.0.0             | 240.0.0.0        | On-link         | 127.0.0.1       | 331    |
| 224.0.0.0             | 240.0.0.0        | On-link         | 192.168.56.1    | 281    |
| 224.0.0.0             | 240.0.0.0        | On-link         | 192.168.6.195   | 291    |
| 255.255.255.255       | 255.255.255.255   | On-link         | 127.0.0.1       | 331    |
| 255.255.255.255       | 255.255.255.255   | On-link         | 192.168.56.1    | 281    |
| 255.255.255.255       | 255.255.255.255   | On-link         | 192.168.6.195   | 291    |  

Persistent Routes:  
  None  

**IPv6 Route Table**   

| If  | Metric | Network Destination                     | Gateway  |
|-----|--------|------------------------------------------|----------|
| 1   | 331    | ::1/128                                  | On-link  |
| 22  | 281    | fe80::/64                                | On-link  |
| 18  | 291    | fe80::/64                                | On-link  |
| 22  | 281    | fe80::2685:78ae:9c3:757a/128             | On-link  |
| 18  | 291    | fe80::797a:1e77:d3f7:589d/128            | On-link  |
| 1   | 331    | ff00::/8                                 | On-link  |
| 22  | 281    | ff00::/8                                 | On-link  |
| 18  | 291    | ff00::/8                                 | On-link  | 

Persistent Routes:  
  None  
  
**Aktuális hálózati kapcsolatok**  
![kiepitett kapcsolatok](https://github.com/user-attachments/assets/d6de3793-001d-4544-a6f2-45547a9accad)

**DNS aktualizálása**  
![dns aktu](https://github.com/user-attachments/assets/91aebf8e-61dd-4701-a14e-12572f207763)

**Hálózati meghajtók listája**  
![meghajtok](https://github.com/user-attachments/assets/d085872e-712a-4f8d-9d2c-95b080c0aba2)

**Ipon.hu szerver tartományneve és ip címe**  
![tartomany nev](https://github.com/user-attachments/assets/f8dd8c25-18be-481e-843b-41709f087397)

**FQDN**  
![fqdn](https://github.com/user-attachments/assets/6a89b30a-418b-45f2-a45e-35fb7f16afbd)

**Sávszélesség teszt**  
![savszelmeres](https://github.com/user-attachments/assets/243afac6-5e0f-4e3e-9ecd-3ff541e210fe)

**WiFi analizer**  
![wifianalizer](https://github.com/user-attachments/assets/32ecb07e-fdac-4b82-8f22-97a8bee445c7)

----
## Egyéb megjegyzések és tapasztalatok  
