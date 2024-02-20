# :potable_water: Controlul nivelului din rezervoare

Standul didactic Festo este o instalaţie compactă şi este proiectat pentru a satisface diferite necesităţi de instruire orientată pe aplicaţii industriale şi o bună cunoaştere a componentelor hardware utilizate în sistemele de control industriale. Standul este conceput pentru realizarea a patru sisteme de control automat, fiecare cu senzorii şi elementele de execuţie aferente: controlul nivelului, controlul debitului, controlul temperaturii, şi controlul presiunii.

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


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# :potable_water: Tanks Level Control System

The didactic stand developed by Festo is a compact installation designed to meet various needs for application-oriented industrial training and provide a good understanding of the hardware components used in industrial control systems. The stand is designed to implement four automatic control systems: level control, flow control, temperature control, and pressure control.

## System Description
The system consists of two water tanks with the same cross-sectional area, positioned one above the other so that the minimum level in the upper tank is at the same level as the maximum level in the lower tank. The upper tank (Reservoir 1) regulates the water level, while the lower tank (Reservoir 2) serves as a buffer tank. The choice of this design makes the pump's task represented by the vertical distance between the water surface in the upper tank and the water surface in the lower tank, i.e., twice the height of the water column in the main reservoir.

## Components
Two water reservoirs
Ultrasonic analog sensor
Flow sensors
Pump motor control amplifier
Signal converters: current to voltage, frequency to voltage
Programmable Logic Controller (PLC)
Control panel
Pipe system
Manual valves
Solenoid valves
System Image

<img width="214" alt="Captură de ecran din 2024-02-20 la 13 18 44" src="https://github.com/chiriacdaria/tanks-level-control/assets/99746700/2de33f32-a22e-4e2b-9a69-f53dff4c07c3">

## Control System
The level regulator is implemented on a PLC, and the resulting control signal is applied to the input of the amplifier, which adjusts the motor pump's supply voltage. The DC motor drives the pump, introducing liquid into the main reservoir. The liquid enters the main reservoir with the inlet flow rate qi and is evacuated with the outlet flow rate qe. Manual valves V101 and V112 control the two flows, qi (V101) and qe (V112). The liquid level in the main reservoir is monitored using an ultrasonic level sensor (LT - Level Transmitter).

## Control Objectives
The project's goal is the automatic regulation of the water level in the main reservoir. The implemented control strategies aim to maintain the level at the prescribed value and quickly reject disturbances. Disturbances can occur through changes in the position of valve V101 (for input flow disturbance) or valve V112 (for output flow disturbance), leading to changes in flow rates.

## Process Control
The input variable to the process is the control voltage of the amplifier, and the output variable from the process is the water level in the main reservoir. The project focuses on stabilizing the water level even when disturbances affect the input or output flow rates.

## Installation Scheme
<img width="680" alt="Captură de ecran din 2024-02-20 la 13 20 10" src="https://github.com/chiriacdaria/tanks-level-control/assets/99746700/86843017-cf4e-4cab-9c80-a034d4f611e8">

The final model of the process consists of individual models for each component block.
