# E-ITS 2024 kataloogirakendus


## Rakenduse käivitamine

a) ```kataloog.html``` fail avada läbi IDE nagu näidatud alloleval pildil
![Avamine IDE kaudu](media/open-using-ide.png)

b) Avada projekti juurkaust ja jooksutada ```http-server .```. Seejärel saab rakendusele ligi ```http://127.0.0.1:8080/kataloog.html```


## Rakenduse funktsionaalsus

Rakendus võimaldab filtreetida tulemusi kasutades allolevaid valikuid:

1. Meetmete filter
   1. Turvameetme tase - kategooriad on dünaamiliselt genereeritud kasutades meetmete sisendfailis olevat ```level``` välja.
   2. Elutsükkel - kategooriad on dünaamiliselt genereeritud kasutades meetmete sisendfailis olevat ```lifecycle``` välja.
   3. C I A - kategooriad on dünaamiliselt genereeritud kasutades meetmete sisendfailis olevat ```cia``` välja.
2. Moodulite filter
   1. Kategooria - kategooriad on dünaamiliselt genereeritud kasutades meetmete sisendfailis olevat ```tags``` välja. Kui väli sisaldab ```sys``` prefiksit kategoriseeritakse ```süsteemimoodulid``` alla. Kui väli sisaldab ```proc``` prefiksit, siis kategoriseeritakse see ```protsessimoodulid``` alla. Kui väli ei sisalda neist kumbagi prefiksit, siis kategoriseeritakse see ```muu``` alla.
   2. Moodulid - kategooriad on dünaamiliselt genereeritud kasutades meetmete sisendfailis olevat ```module``` välja. Kategooriad on loodud kasutades väljade prefikseid enne esimest punkti. 
3. Vastuste filter - loodud käsitsi võttes aluseks näidis-kuvatõmmist kuna nende valikute kohta ei tundu sisendfailides informatsiooni olevat. Määrab millised tunnused kuvatakse tulemustes. 
4. Rollide filter - kategooriad on dünaamiliselt genereeritud kasutades meetmete sisendfailis olevat ```assignee``` välja.
5. Märksõna - võimaldab sisestada teksti vabal kujul. Otsib tulemustest üle ```meetme nimetus``` ja ```meetme sisu``` tunnuste vastavat teksti ja näitab vastavusi tulemustes paksus kirjas.

Tulemuste tabel sisaldab allolevaid tunnuseid (vastavalt vastute filtritele):
1. Mooduli vastutaja - kasutab tulemuste kuvamiseks meetmete sisu failis olevat ```responsible``` välja.
2. Meetme nimetus - kasutab tulemuste kuvamiseks meetmete sisu failis olevaid ```mid``` ja ```title``` väljasid kombineeritult nagu näidis-tulemustes kuvatud.
3. Meetme sisu - kasutab tulemuste kuvamiseks meetmete sisu failis olevat ```content``` välja.
4. Kaasvastutaja - kasutab tulemuste kuvamiseks meetmete sisu failis olevat ```assignee``` välja.
5. Meetme alusohud - kasutab tulemuste kuvamiseks meetmete failis olevat ```threats``` välja. Tulemuste loomiseks on kombineeritud meetmete failis ja meetmete sisu failis vastavalt ```measure``` ja ```mid``` väljad ning kasutades neid on tulemustele pandud külge ```threats``` väli.
6. ISO27001 vastavus - kasutab tulemuste kuvamiseks meetmete failis olevat ```iso``` välja. Tulemuste loomiseks on kombineeritud meetmete failis ja meetmete sisu failis vastavalt ```measure``` ja ```mid``` väljad ning kasutades neid on tulemustele pandud külge ```iso``` väli.
7. Meetme tase - kasutab tulemuste kuvamiseks meetmete sisu failis olevat ```level``` välja.
8. Meetme elutsükkel - kasutab tulemuste kuvamiseks meetmete sisu failis olevat ```lifecycle``` välja.
