# PLC_Delta_Motor
PLC Motor Start-Stop

Projekt elektryczny realizujący proces uruchamiania silnika trójfazowego z sieci sztywnej w wybranych konfiguracjach. Cechy środowiskowe pracy silnika:

•	Połączenie uzwojeń silnika w trójkąt.<br />
•	Zasilanie silnika z sieci sztywnej 3x400V.<br />
•	Brak zastosowanej przekładni mechanicznej.<br />
•	Napędzanie taśmociągu (niski moment obciążenia).<br />
•	Logika sterowania realizowana jest z udziałem sterownika PLC.<br />
•	Środowisko pracy o niskim rygorze ze względu na warunki bezpieczeństwa.<br />
•	Dwukierunkowe praca silnika.<br />
•	Zaimplementowane zabezpieczenia: termalne, nadmiaroprądowe oraz przycisk awaryjny.<br />
•	Układ Start-Stop.<br />

Dane znamionowe silnika indukcyjnego:

•	Współczynnik mocy: 0.68<br />
•	Przekładnia wewnętrzna: 20:1<br />
•	Liczba obrotów na minutę: 1350 rpm<br />
•	Prąd znamionowy: 0.7A/0.4A<br />
•	Napięcie znamionowe: 230V/400V<br />

Wykorzystane rekwizyty:

•	Trzy przyciski monostabilne.<br />
•	Przycisk bezpieczeństwa.<br />
•	Sterownik PLC z serii Delta DVP28SV.<br />
•	Termik w układzie NC.<br />
•	Dwa styczniki z serii Siemens Sirius z dodatkowymi stykami NC.<br />
•	Zasilacz 24V o mocy 30W.<br />
•	Wyłącznik silnikowy Siemens 0.75-1A. Nastawiony na 0.8A<br />
•	Żarówka 8W 24VDC.<br />
•	Przełącznik krzywkowy 2-pozycyjny 1xNO.<br />

Oznaczenia rekwizytów na schemacie:

|Lp|	Indeks|	Opis|
| --- | --- | --- |
|1|	M1|	Silnik 3x400V|
|2|	Q1|	Wyłącznik silnikowy|
|3|	K1/K2|	Praca silnika do przodu / do tyłu|
|4|	S3/S2|	Przycisk Start / Stop|
|5|	S4|	Przełącznik krzywkowy|
|6|	T1|	Wyłącznik termiczny|
|7|	SG|	Wyłącznik bezpieczeństwa|
|8|	H1|	Sygnalizacja błędu|
|9|	8A|	Bezpieczniki topikowe 8A|
|10|	PLC|	Sterownik PLC DVP28SV|

Oznaczenie wejść/wyjść cyfrowych:

|Lp|	I/O|	Opis|
| --- | --- | --- |
|1|	X0|	Start|
|2|	X1|	Stop|
|3|	X2|	Do przodu / Do tyłu|
|4|	X5|	Kasacja błedu|
|5|	X6|	Termik|
|6|	X7|	Wyłącznik bezpieczeństwa|
|7|	Y0|	Do przodu|
|8|	Y1|	Do tyłu|
|9|	Y2| 	Sygnalizacja błędu|
|10|	C1, C2, C3|	Potencjały wspólne|

Schemat elektryczny sterowania:
![PLC_Motor](img/PLC_Motor.png)

Sekcja inicjacyjna PLC:
![1](https://github.com/cheapmouse94/PLC_Delta_Motor_pl/assets/75945631/4e8ef065-a53f-4cda-bf85-a05a0b5ed5f3)

Sekcja logiczna PLC:
![2](https://github.com/cheapmouse94/PLC_Delta_Motor_pl/assets/75945631/ccb5c126-2509-4da9-a256-291d9066ba54)




