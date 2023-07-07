Cel projektu: 
Naszym celem jest zaprognozowanie całkowitej liczby zachorowań w Polsce na Covid-19 w dniach 20-26.04.2023 na podstawie historycznych danych (wybraliśmy dane do 13.04.2023).<br>

metodologia:
prognozujemy ilość zachorowań na bazie własnych spostrzeżeń. Zauważyliśmy, że funkcja zakażeń zachowuje się okresowo - liczba zachorowań rośnie jesienię i wiosną, a maleje latem oraz zimą. Chcemy zatem przenieść tempo zmian zachorowań z tego samego okresu z poprzedniego roku i odpowiednio je przeskalować do aktualnych danych. Dodatkowo prognozy dokonujemy dla każdego dnia osobno, tj. czwartki prognozujemy tylko na podstawie czwartków itd.<br>
<br>
<br>


opis działania kodu:<br>
1) wczytanie ogólnej liczby zakażeń do tablicy liczba_przypadkow<br>
2)podzielenie danych z tablicy liczba_przypadkow na poszczególne dni tygodnia<br>
następnie dla kazdego dnia tygodnia:<br>
3)policzenie średniej z 8 tygodni z przedniego roku<br>
4)policzenie współczynnika a_dzien_tygodnia - odpowiedzialny za tempo wzrostu oraz rosnącą (a_dt>0) lub malejącą (a_dt<0)liczbę przypadków<br>
5)wyznaczenie prognozowanej liczby przypadków ze wzoru: <br>
    prognoza=ostatni_dzień + 7a_dt(ostatni_dzień/średnia) <br>
6)od piątku do środy kroki 4 i 5 są wykonywane 2 razy (potrzeba dodatkowego prognozowania zakażeń od 14.04 do 19.04)<br>
7)dla czwratku po pierwszym korku odrazu dostajemy zakażenia z 20.04<br>
8)zakażenia od 14.04 do 26.04 są wypisane w ostatniej komórce<br>

Wnioski:<br>
-Wielkanoc co była teraz trochę zaniży przewidywane zachorowania z poniedziałku i może wtorku<br>

Bibliografia:<br>
dane pobraliśmy ze strony:<br>
https://www.gov.pl/web/koronawirus/wykaz-zarazen-koronawirusem-sars-cov-2