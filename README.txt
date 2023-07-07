Cel projektu: 
Naszym celem jest zaprognozowanie całkowitej liczby zachorowań w Polsce na Covid-19 w dniach 14-26.04.2023 na podstawie historycznych danych (wybraliśmy dane do 13.04.2023).

Metodologia:
Prognozujemy ilość zachorowań na bazie własnych spostrzeżeń. Zauważyliśmy, że funkcja zakażeń zachowuje się okresowo - liczba zachorowań rośnie jesienię i wiosną, a maleje latem oraz zimą. Chcemy zatem przenieść tempo zmian zachorowań z tego samego okresu z poprzedniego roku i odpowiednio je przeskalować do aktualnych danych. Dodatkowo prognozy dokonujemy dla każdego dnia osobno, tj. czwartki prognozujemy tylko na podstawie czwartków itd.
Program został napisany w języku Python.


opis działania kodu:
1) wczytanie ogólnej liczby zakażeń do tablicy liczba_przypadkow
2)podzielenie danych z tablicy liczba_przypadkow na poszczególne dni tygodnia
następnie dla kazdego dnia tygodnia:
3)policzenie średniej z 8 tygodni z przedniego roku
4)policzenie współczynnika a_dzien_tygodnia - odpowiedzialny za tempo wzrostu oraz rosnącą (a_dt>0) lub malejącą (a_dt<0)liczbę przypadków
5)wyznaczenie prognozowanej liczby przypadków ze wzoru: 
    prognoza=ostatni_dzień + 7a_dt(ostatni_dzień/średnia) 
6)od piątku do środy kroki 4 i 5 są wykonywane 2 razy (potrzeba dodatkowego prognozowania zakażeń od 14.04 do 19.04)
7)dla czwratku po pierwszym korku odrazu dostajemy zakażenia z 20.04
8)zakażenia od 14.04 do 26.04 są wypisane w ostatniej komórce

Wnioski:
-Wielkanoc co była teraz trochę zaniży przewidywane zachorowania z poniedziałku i może wtorku,
-Po porównaniu z danymi udostępnianymi na oficjalnych stronach rządowych możemy zauważyć, że błąd oszacowań to średnio 37%.

Bibliografia:
dane pobraliśmy ze strony:
https://www.gov.pl/web/koronawirus/wykaz-zarazen-koronawirusem-sars-cov-2
