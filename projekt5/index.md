# MÉRÉSI JEGYZŐKÖNYV

**A mérést végző neve:** Csépke Péter  
**A mérés tárgya:** Bitsebesség vs jelminőség mérési feladat  
**A mérés dátuma:** 2024.11.27.  
**A mérést vezette:** Sándor Péter  
**Évfolyam:** 13. E  
**Csoport:** GYAK 2  
**Helyszín:** V3  

---

## A mérés menete 
   - Összekábeleztem a modulátorokat egymásba fűzve, majd a kör végén található modulátor RF kimenetét összecsatlakoztattam a Spektrumanalizátorra.  
   - Gyári beállításokra visszaállítottam a modulátorokat (Factory Reset).  
   - A hardver vezérlőfelületén keresztül beállítottam a modulátort. Kiválasztottam két külön testre szabott RF frekvenciát (pl. 594 MHz, 602 MHz).  
   - Beállítottam a többcsatornás jelkimenetet: két különálló programot (pl. TV1 és TV2 néven átnevezve a modulátor beállításában).  
      - Moduláció: 64-QAM.
      - Sávszélesség: 8 MHz.
   - Az RF kábelen keresztül csatlakoztattam a DVB-T vevőt a modulátorhoz, és ellenőriztem, hogy mindkét program helyesen vehető-e a METEK HD spektrum/jelszint analizátorral.
   - Választottam két eltérő bitsebességet a két program számára:
     - TV1: 15 Mbps
     - TV2: 10 Mbps  
   - Végezetül táblázatba kigyűjtöttem a mért adatokat.  

 ### Összeszerelés után
 <p align="center">
   <img src="https://github.com/user-attachments/assets/12b4b172-3480-446c-98d7-5a1b389832a2" width="600" height="400">
 </p>

---

## Alkalmazott mérőeszközök és készülékek  

| Műszer neve | Típus          | Gyártási szám |
| ---------------- | ---------------- | -------------- | 
| Johansson 8202      | HDMI Modulator     | 2341010237801         | 
|       Johansson 8202            | HDMI Modulator   | 2341010237504     |
|           METEK HDD       | Spektrum analizátor | 211112002390         | 
| Laptop    | HP      | 3.        | 
 
---

## A mért értékek

| Mérési paraméter   | RF frekvencia (MHz) | Program neve | Bitsebesség (Mbps) | Jelszint (dBm) | MER érték (dB) |
|--------------------|---------------------|--------------|--------------------|----------------|----------------|
| **Mérési eredmény 1** | 594              | TV1          | 15                 | -35.1             | 40             |
| **Mérési eredmény 2** | 602              | TV2          | 10                 | -29.4             | 35.4             |
| **Mérési eredmény 3** | 602              | TV2          | 21.5 (max)         | -29.6             | 35.4             |

---

## Mérési eredmények elemzése
Az adatok alapján az alábbi következtetéseket lehet levonni:
A táblázat adatai alapján az látszik, hogy a TV1 ami a TV2-be csatlakozik majd a spektrum analizátorba veszteséges a másikhoz képest ami valószínüleg az RF kábel lehet. Illetve a TV2 10 illetve 21.5(max) bitsebessége között nincs nagy eltérés azonban a beérkező bitrátában látszott a változás.  
<p aling="center">
  <img src="https://github.com/user-attachments/assets/d5af8eec-9495-4f17-a03b-5d7f99ba76fe" width="600" height="350">
</p>  
<p align="center"><strong>TV1 jele</strong></p>

<p aling="center">
  <img src="" width="600" height="350">
</p>  
<p align="center"><strong>TV2 10Mbps-en</strong></p>

<p aling="center">
  <img src="" width="600" height="350">
</p>  
<p align="center"><strong>TV2 21,5Mbps-en</strong></p>

---

## Konklúzió  
Összességében, a mérések alapján a Johansson 8202 DVB-T modulátor képes stabilan kezelni a különböző bitsebességeket, de a jelminőség és a jelszint optimalizálásához figyelembe kell venni a kábelezést. A modulátor többcsatornás működése során a bitsebesség növelése nem eredményezett drámai csökkenést a jelminőségben  

---

## Javaslatok  
A modulátorokon a feladat kezdetén mindenképpen csináljatok egy factory resetet hogy ne ütközzetek más beállításokba. Ha a spektrum analizátoron hasonló jelszintet szeretnétek mérni. Akkor a TV1-en erősíteni kell a kimeneten számolva a kábelen történő veszteséggel.  

---

<br>

**Aláírás:** ...

**Dátum:** ...
