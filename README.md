# Prvi projektni zadatak iz predmeta "Mikrokontrolerskih sistemi"

Postavka zadatka:
	Koristimo slova iz sopstvenog imena i prezimena da bismo izabrali konfiguracije na mikrokontroleru.
	1) Ako ime i prezime u sebi imaju više samoglasnika, onda koristimo pin A. U suprotnom pin B.
	2) Broj pina koji koristimo je zbir svih slova u imenu i prezimenu po modulu 6.
	3) Širina impulsa je jednaka broju slova u imenu u sekundama, a širina pauze je jednaka broju slova u 
	   prezimenu u sekundama.
	4) Impulsni odziv se ponavlja onoliko puta koliko ima slova u imenu, posle čega se vrednosti širine
	   impulsa i širine pauze "zamenjuju". Ovakav impulsni odziv se ponavlja onoliko puta koliko ima slova
	   u prezimenu, posle čega se opet širine i ponavljanja opet vraćaju u prvobitno stanje i tako u krug.


1) Pin A ili pin B:

  Moje ime i prezime: Mijačić Tamara
	Tamara => 3 samoglasnika, 3 suglasnika
	Mijačić => 3 samoglasnika, 4 suglasnika

	*Na osnovu ovoga uzima se pin B.

2) Broj pina koji koristimo:
	( 6 + 7 ) % 6 = 1

	*Koristimo pin PB1.

3) Širina impulsa i širina pauze:
	Prvi slučaj: 6s - impuls
		     7s - pauza
	Drugi slučaj: 7s - impuls
		      6s - pauza


4) Na osnovu stavke broj 3):
	*Prvi slučaj se ponavlja 6 puta
	*Drugi slučaj se ponavlja 7 puta
