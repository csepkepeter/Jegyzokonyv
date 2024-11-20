# MÉRÉSI JEGYZŐKÖNYV

**A mérést végző neve:** Csépke Péter, Horváth Martin  
**A mérés tárgya:** A különböző frekvenciák és modulációk miként befolyásolják a jelminőséget.  
**A mérés száma:** 03  
**A mérés dátuma:** 2024. 10. 09.  
**A mérést vezette:** Sándor Péter

---

**Aláírás:**  
**Évfolyam:** 13. E  
**Csoport:** GYAK 1  
**Helyszín:** V3 Labor  
**Beadás dátuma:** 2024. 10. 09.  
**Osztályzat:**

---

## A mérés menete és célja:

**Cél:**  
A tanulók megismerjék a Johansson 8202 DVB-T modulátor működését, konfigurációs lehetőségeit, és méréseket végezzenek a METEK HD spektrum/jelszint analizátorral. A mérési eredményeket rögzítik jegyzőkönyv formájában.

**Menete:**  
1. Előkészítettük a megfelelő műszereket a mérés végzéséhez.
2. Összecsatlakoztattuk a METEK HD spektrum/jelszint analizátort a Johansson 8202 HDMI modulátorral.
3. Beállítottuk a Johansson 8202 HDMI modulátort az adott frekvencia sávokra.
4. A METEK HD analizátorral rááltunk a modulátorral létrehozott sávokra.
5. Egy adott frekvencián három féle moduláció típust használtunk a jelszint, bitsebesség, MER érték meghatározására.
6. A kapott adatokat egy táblázatban összegyűjtöttük.

---

## Mérési eszközök:

| Műszer neve                       | Típus                     | Gyártási szám        | Mérési tartomány | Mérési határok     | Kép |
|-----------------------------------|---------------------------|----------------------|------------------|--------------------|-----|
| Johansson Hdmi modulátor          | 8202                      | 2341010237504        | 17-1218 MHz      |                    | <img src="https://github.com/csepkepeter/Jegyzokonyv/blob/main/projekt3/hdmi%20modulator.png" widht="150" height="100">    |
| METEK HD spektrum/jelszint analizátor | —                        | 240002               | 50-2200 MHz      | 51 MHz - 1000 MHz   | <img src="https://github.com/csepkepeter/Jegyzokonyv/blob/main/projekt3/metekhd.png" width="150" height="100">    |
| Laptop                            | HP                        | —                    | —                | —                  |     |

---

## Adattáblázat:

| Mérési paraméter      | RF Frekvencia (MHz) | Moduláció típusai | Sávszélesség (MHz) | Jelszint (dBm) | Bitsebesség (Mbps) | MER érték (dB) |
|-----------------------|---------------------|-------------------|--------------------|----------------|--------------------|----------------|
| **Mérési eredmény 1**  | 212                 | 64 QAM            | 7                  | -29.6          | 15.8               | 38.3           |
| **Mérési eredmény 2**  | 212                 | 16 QAM            | 7                  | -29.4          | 7.8                | 36.4           |
| **Mérési eredmény 3**  | 212                 | QPSK              | 7                  | -29.4          | 3.7                | 39.9           |
| **Mérési eredmény 1**  | 474                 | 64 QAM            | 8                  | -31            | 18                 | 36.8           |
| **Mérési eredmény 2**  | 474                 | 16 QAM            | 8                  | -30.7          | 9.1                | 35.3           |
| **Mérési eredmény 3**  | 474                 | QPSK              | 8                  | -30.4          | 4.2                | 39.4           |
| **Mérési eredmény 1**  | 546                 | 64 QAM            | 8                  | -30.3          | 18.3               | 36.1           |
| **Mérési eredmény 2**  | 546                 | 16 QAM            | 8                  | -30.2          | 9.2                | 35.8           |
| **Mérési eredmény 3**  | 546                 | QPSK              | 8                  | -31            | 4.3                | 39.9           |

---

## Mérések többféle modulációval:  

<p align="center">
  <img src="https://github.com/csepkepeter/Jegyzokonyv/blob/main/projekt3/64qam.png" width="600" height="350">
</p>
<p align="center"><strong>1. ábra: 64 QAM</strong></p>

<p align="center">
  <img src="https://github.com/csepkepeter/Jegyzokonyv/blob/main/projekt3/16qam.png" width="600" height="350">
</p>
<p align="center"><strong>2. ábra: 16 QAM</strong></p>

### 3. ábra: QPSK

---

## Következtetések:

A mérések alapján megállapítható, hogy a 64-QAM moduláció a legmagasabb adatsebességet biztosít, viszont a jelkódolás minősége (MER) alacsonyabb, mint a kisebb modulációs rendeknél, mint például a 16-QAM és a QPSK. Ezzel szemben a QPSK moduláció kiváló MER értékeket mutatott, de a bitsebessége jelentősen alacsonyabb volt.

