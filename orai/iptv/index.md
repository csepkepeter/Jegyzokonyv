# MÉRÉSI JEGYZŐKÖNYV
# Méréstechnikai Feladat: IPTV vételi rendszer kiépítése  

**A mérést végző neve:** Csépke Péter  
**A mérés tárgya:** IPTV vételi rendszer kiépítése  
**A mérés száma:** órai mérés 03.  
**A mérés dátuma:** 2025.02.03.  
**A mérést vezette:** Sándor Péter  

**Évfolyam:** 13. E  
**Csoport:** GYAK 1  
**Helyszín:** V3 Labor  

### A mérés célja  
A földfelszíni digitális TV vételi rendszer kiépítése, a megfelelő adótorony kiválasztása, a jel mérésének és elosztásának elvégzése, és az IPTV rendszer konfigurálása.  

### Méréshez használt eszközök  

1. Antenna: Kültéri antenna (Iskra P2845)  
2. Fejállomás: LEMCO SCL-824CT (8darab bemenet, 4darab kimenet)  
3. Set-top box: MAG IPTV  
4. Hálózati eszköz: TP-Llink Archer C7   
5. METEK HDD digitális jelmérő  
6. Koaxiális kábelek és csatlakozók  
7. Jelosztó: Ekselans RF16  osztó 5-2400MHz  
8. UTP kábelek  
9. Szerelési eszközök: csavarhúzó, villáskulcs, kábelvágó, iránytű  

|     Műszer neve    |        Típus        |      Kép      |
| ------------------ | ------------------- | --------------| 
| Antenna            | Iskra P2845         |               | 
| Fejállomás         | LEMCO SCL-824CT     |               | 
| Set-top box        | MAG IPTV            |               | 
| Laptop             | HP                  |               | 
| Router             | TP-Link Archer C7   |               |
| Spektrumanalizátor | METEK HDD           |               |
| Jelosztó           | Ekselans RF16       |               |

-----

## A feladat menete  
Mielőtt elkeztem volna a hálózat kiépítését és konfigurálását minden eszközt alaphelyzetbe állítottam, hogy az esetleges zavaró tényezők megszünjenek.
Ezt követően felléptem az **fmdx.hu** oldalára és megkerestem az avasi adótorony csatornakiosztását.  

Keresgéltem az ingyenes csatornák közül és kiválasztottam a digitális földfelszíni televízióadások közül a **Miskolc Városi TV** -t, ami a **634MHz-en** helyezkedik el. A választásom azért esett erre, mert ezt a csatorna sugároz a leggyengébben **(0,126kW)**, és ezt a csatornát sikerül a legerősebb vétellel venni akkor a többi csatorna is optimális jellel fogható.  

![miskolctv](https://github.com/user-attachments/assets/cc053a97-7acb-4da9-b6f4-d5dbd3e8bf70)  

Mivel a környezeti tényezők befolyásolhatják a vett jel erősségét így az adott viszonyokhoz próbáltam a lehető legnagyobb jelerősséget beállítani;  

Az akkori tényezők:  
- Páratartalom: 68%   
- Légnyomás: 1027 mBar  
- Hőmérséklet: 5°C  
- Szélerősség: 3,2 m/s

Végül az antenna szögállása: Délnyugat 234°  

### Spekrtumanalizátor adatai  

- Jelszint: 50.3dB  
- Noise Margin: 19.8  
- MER érték: 26.3dB  
- Moduláció: DVBT/QPSK/8K/1/32  
![metek](https://github.com/user-attachments/assets/cec8dcc8-1797-44ee-9447-d736db48ff49)

### A fejállomás konfigurálása  

Mivel egyetlen antenna jelet osztottam négy külön részre, így lehetséges volt, hogy az elosztott jel erőssége jelentősen csökkenhet, de mivel egy erősebb, magasabb nyereségű antennát használtam, így ez a probléma nem lépett fel.  
Megkerestem az ingyenesen fogható csatornákat, amikből a legtöbbet rögzítettem a fejállomás bementeire.   
Aztán beállítottam a laptop interfészét, amelynek a Lemco IP címével kellett egyeznie. Ebben az esetben a 192.168.1.1 /24-es tartományt állítottam be, és az alapértelmezett átjárót 192.168.1.200-ra.  
A LEMCO alap IP címe tehát 192.168.1.200. Az alapértelmezett neve **admin** és jelszava **12345**.  

A táblázat alapján az **Input 1** lett a **multiplex A**;  

![mpa](https://github.com/user-attachments/assets/3555920a-57e7-4d24-9a31-56fd4105859e)  

Az **Input 2** a **multiplex B**;  

![mpb](https://github.com/user-attachments/assets/0529447d-2de4-4d5f-9dfe-84f51b4aaf20)  

Az **Input 7** lett a **Miskolc Város TV**;  

![mptv](https://github.com/user-attachments/assets/a6ccd5be-e625-4029-96ac-3714a24d8208)  

Végezetül az **Input 8** lett a **multiplex E**.  

![mpe](https://github.com/user-attachments/assets/eb2ab7ef-d240-45da-a065-82e683e07b0f)  

### A router konfigurálása  

Bekapcsoltam az **IGMP-snooping** protokollt, hogy megakadályozzuk a helyi hálózat állomásait abban, hogy forgalmat fogadjanak olyan eszközről, amire kifejezetten nem csatlakoztak.  
A bemenetet, kimenetet és a laptop interfészét is IPTV-re állíttottam.  
Beállítottam, hogy DHCP szervert osszon, ami **192.168.1.100**-tól oszt IP-t **192.169.1.249**-ig. Az alapértelmezett átjárója pedig **192.168.1.1**.  
Végezetül bridgeltem LAN1-ről LAN3-ra közvetlenül IPTV-ről.  

----

## Tesztelések és mérési eredmények  

A táblázat összegzi a televíziós és rádiós csatornák adatait, a csatornák neveit, azonosítóit, logikai csatorna számát, IP-címét, portját és az adatátviteli protokollt. Ezek az adatok a csatornák jellemzőit és hozzáférhetőségét foglalja össze.  

| Input | Program title              | OriginalService ID   | LCN1..1023 | Encrypted | TS Output | OutputService ID | IP address    | IP port | Protocol |
|-------|----------------------------|----------------------|------------|-----------|-----------|------------------|---------------|---------|----------|
| 1     | Input 1                    | M1 HD                | 100        | 0         | FTA       | 1                | 224.0.0.1     | 1001    | UDP      |
| 2     | Input 1                    | M4 Sport HD          | 101        | 0         | FTA       | 1                | 224.0.0.1     | 1002    | UDP      |
| 3     | Input 1                    | Duna HD              | 102        | 0         | FTA       | 1                | 224.0.0.1     | 1003    | UDP      |
| 4     | Input 1                    | DunaW/M4Sport+       | 103        | 0         | FTA       | 2                | 224.0.0.1     | 1004    | UDP      |
| 5     | Input 1                    | Kossuth Radio        | 130        | 0         | FTA       | 4                | 224.0.0.1     | 1005    | UDP      |
| 6     | Input 1                    | Petofi Radio         | 131        | 0         | FTA       | 4                | 224.0.0.1     | 1006    | UDP      |
| 7     | Input 1                    | Bartok Radio         | 132        | 0         | FTA       | 4                | 224.0.0.1     | 1007    | UDP      |
| 8     | Input 1                    | Danko Radio          | 133        | 0         | FTA       | 4                | 224.0.0.1     | 1008    | UDP      |
| 10    | Input 2                    | M2 HD                | 200        | 0         | FTA       | 1                | 224.0.0.1     | 1010    | UDP      |
| 11    | Input 2                    | M5 HD                | 201        | 0         | FTA       | 2                | 224.0.0.1     | 1011    | UDP      |
| 12    | Input 2                    | TV2                  | 202        | 0         | FTA       | 1                | 224.0.0.1     | 1012    | UDP      |
| 13    | Input 2                    | RTL                  | 203        | 0         | FTA       | 1                | 224.0.0.1     | 1013    | UDP      |
| 14    | Input 2                    | MAX4                 | 206        | 0         | FTA       | 2                | 224.0.0.1     | 1014    | UDP      |
| 15    | Input 2                    | Spektrum Home +      | 207        | 0         | FTA       | 2                | 224.0.0.1     | 1015    | UDP      |
| 16    | Input 2                    | MinDig TV Plusz Info | 208        | 0         | FTA       | 2                | 224.0.0.1     | 1016    | UDP      |
| 37    | Input 3                    | HEVC teszt           | 524        | 0         | FTA       | 2                | 224.0.0.1     | 1037    | UDP      |
| 39    | Input 4                    | Miskolc TV           | 1000       | 0         | FTA       | 2                | 224.0.0.1     | 1039    | UDP      |  

**8 MHz sávszélességgel sugároz mindegyik csatorna.**  

-----

## Hibakeresés:    

Nem tudtam elérni a konfigugációs oldalt, mint kiderült nem volt rendesen bedugva az UTP kábel.   
Nem volt M1, ezért újra kellett konfigurálni az input 1-en lévő 634 MHz csatornát 666 MHz-re.   
1000 - 1023-ig a portkiosztást nem fogadta el, 1024-től lehet kiosztani a portokat ahhoz, hogy működjön.  
224.0.0.1-es IP cím nem jó, mivel ez egy link-local cím és csak .2-től működik a kiosztás.  
