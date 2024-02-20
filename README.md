Standul didactic Festo (Figura 1.1) este o instalaţie compactă şi este proiectat pentru a satisface diferite necesităţi de instruire orientată pe aplicaţii industriale şi o bună cunoaştere a componentelor hardware utilizate în sistemele de control industriale. Standul este conceput pentru realizarea a patru sisteme de control automat, fiecare cu senzorii şi elementele de execuţie aferente: controlul nivelului, controlul debitului, controlul temperaturii, şi controlul presiunii.

Sistemul conține două rezervoare de apă, cu aceeași secțiune transversală, situate unul deasupra celuilalt astfel încât minimul.
în rezervorul de sus este la același nivel cu maximul din rezervorul de jos. Nivelul este reglat în Rezervorul 1, iar Rezervorul 2 are rolul de rezervor tampon. 
Rezervorul în care se reglează nivelul este poziționat deasupra rezervorului tampon. Prin alegerea acestei soluții constructive sarcina pompei este reprezentată de distanța pe verticală dintre suprafața apei în rezervorul de sus și suprafața apei în cel de jos, adică de două ori înălțimea coloanei de apă din rezervorul principal.
Pentru nivelul minim în rezervorul principal, rezervorul tampon este plin, suprafața apei în acest caz în cele două rezervoare fiind aproximativ pe același nivel.
Alte componente ale staţiei Festo utilizate pentru controlul nivelului sunt: senzor ultrasonic analogic, senzori de debit, amplificatorul pentru comanda motorului pompei, convertoare de semnale: din curent în tensiune, din frecvenţă în tensiune, PLC, panou de control, sistem de conducte de legătură, valve manuale, electrovalve.

<img width="214" alt="Captură de ecran din 2024-02-20 la 13 18 44" src="https://github.com/chiriacdaria/tanks-level-control/assets/99746700/2de33f32-a22e-4e2b-9a69-f53dff4c07c3">

Regulatorul de nivel este implementat pe un PLC iar semnalul de comandă rezultat este aplicat la intrarea amplificatorului care va modifica corespunzător tensiunea de alimentare a motorului pompei, motor de curent continuu. Motorul antrenează pompa care introduce lichid în rezervorul principal. În rezervorul principal intră lichid cu debitul qi și este evacuat cu debitul qe. V101 și V112 sunt valve acționate manual de care depind cele două debite qi (V101) și qe (V112). Nivelul lichidului în rezervorul principal este monitorizat cu ajutorul unui senzor de nivel ultrasonic (LT- Level Transmitter). Valoarea dată de senzor este valoarea actuală a nivelului în rezervor.
Variabila de intrare în proces este tensiunea de comandă a amplificatorului, iar variabila de ieșire din proces este nivelul apei din rezervorul principal.
Scopul proiectului este reglarea automată a nivelului din rezervorul principal. Trebuie implementate strategii de control care au ca scop menţinerea nivelului la valoarea prescrisă și rejectarea rapidă a perturbațiilor.
Când procesul ajunge în regim staționar, înălțimea coloanei de apă în rezervor este constantă (debitul de intrare qi este egal cu debitul de ieșire qe). În cazul unei reglări de stabilizare, această valoare trebuie menținută la un nivel fix chiar dacă apar perturbații de debit pe
conducta de evacuare sau intrare. Perturbațiile pot apărea prin modificarea poziţiei robinetului V101 (pentru perturbația pe debitul de intrare) sau modificarea robinetului V112 (pentru perturbația pe debitul de ieșire) care duc la modificarea debitelor.
Schema simplificată a instalației este prezentată în figura.
<img width="680" alt="Captură de ecran din 2024-02-20 la 13 20 10" src="https://github.com/chiriacdaria/tanks-level-control/assets/99746700/86843017-cf4e-4cab-9c80-a034d4f611e8">

Modelul final al procesului va fi compus din modelele individuale pentru fiecare bloc component.
