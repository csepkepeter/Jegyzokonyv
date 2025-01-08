# MÉRÉSI JEGYZŐKÖNYV   
## Méréstechnikai Feladat: Tranzisztor működésének vizsgálata  
A mérést végző neve: Csépke Péter
A mérés tárgya: Tranzisztor működésének vizsgálata  
A mérés száma: 05. mérés  
A mérés dátuma: 2025. 01. 08  
A mérést vezette: Sándor Péter  

Évfolyam: 13. E  
Csoport: GYAK 2  
Helyszín: V3 Labor  

## Feladat célja:   
Tranzisztor kimeneti feszültségének és a kollektor áramának kiszámítása a megadott ellenállás értékekkel.  

## Elméleti háttér:   
A tranzisztor egy félvezető eszköz, amelyet elsősorban erősítésre és kapcsolásra használnak az elektronikai áramkörökben. Működése a félvezető anyagok, például szilícium vagy germánium tulajdonságain alapul, amelyek képesek az elektromos áram vezetésére és szigetelésére is, attól függően, hogy milyen típusú szennyező anyagokat adnak hozzá. A tranzisztor három fő részből áll: az emitterből, a bázisból és a kollektorból.   

## Feladatban használt eszközök:   
 - Ellenállások  
     - Rc = 220 Ω  
     - Rbe = 1,5k Ω  
 - Tranzisztor  
     - β = 81  
 - LED  
 - Multiméter:   
     - Metex m-3800 736015  
 - NI MYDAQ  

------

## Falstadban készített áramkör   
<img src='https://github.com/user-attachments/assets/328aadf0-83d5-4f37-9e57-a149318ba7b1' width='550' height='600'>  

## Mérési táblázat 

| Ube [V]   | Urc [V]  | Ic   [mA]  | 
| --------- | -------  | ---------- | 
| 0         | 0        |      0     | 
| 0,1       | 0        |      0     | 
| 0,2       | 0        |     0      | 
| 0,3       | 0        |      0     |
| 0,4       | 0.1m     |    0,14    | 
| 0,5       | 3.1m     |    0,52    | 
| 0,6       | 113,9m   |       4,06 |
| 0,7       | 894      |       9,64 | 
| 0,8       | 2,12     |      11,73 | 
| 0,9       | 2,58     |      11,86 |   
| 1         | 2,61     |      11,95 |   
| 1,1       | 2,63     |        12  |   
| 1,2       | 2,64     |    12,05   |   


## Valóságban összetett áramkör
<img src='https://github.com/user-attachments/assets/90313169-d817-4dc0-ba30-2a76c3bf9ab9' width='550' height='400'>  
<img src='https://github.com/user-attachments/assets/ff1d579d-ebb2-4512-a5e5-34e6d8741b96' width='550' height='400'>  

## Megjegyzések:
A feladat során számos nehézséggel találkoztam, amelyek befolyásolták és lassították a megoldás folyamatát.A nevezetes és a mért adatok nem sokkal tértek el. Megfigyelhető, hogy 0 - 0,5 V-ig az áramkör zárt állásban volt. Mindezek után 0,6V értéknél nyílt ki a tranzisztor és kezdett világítani a LED. 1,2 V értéktől kezdett stabilizálódni és változatlan maradt az ellenálláson eső feszültség.
