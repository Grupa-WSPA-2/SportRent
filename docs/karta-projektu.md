 KARTA PROJEKTU — WERSJA 0.1 

1. Podstawowe informacje 

Nazwa projektu: System wypożyczalni sprzętu sportowego 

Krótka nazwa / akronim: SportRent 

Zespół: 

Imię i nazwisko:   Rola główna:

Nazar Ostapenko - Koordynator 
Bohdan Poderiako - Baza danych/Analiza wymagań 
Kyrylo Skliarov - Backend 
Andriy Rushchak - Frontend/UI/UX 
Rostyslav Svistelnytskyi - Testowanie 

2. Problem 

Jaki problem chcemy rozwiązać? 

Chcemy zrobić system, który będzie pomagał w wypożyczaniu sprzętu sportowego. Będzie można sprawdzić jaki sprzęt jest dostępny i go wypożyczyć. Pracownik będzie mógł dodawać sprzęt, sprawdzać wypożyczenia i przyjmować zwroty. Dzięki temu nie trzeba będzie wszystkiego zapisywać na kartce. 


3. Kogo dotyczy problem? 

Problem dotyczy klientów wypożyczalni oraz pracowników, którzy zajmują się wypożyczaniem sprzętu. 


4. Cel systemu 

Celem systemu jest ułatwienie zarządzania sprzętem sportowym i jego wypożyczaniem. 

System ma pozwalać na sprawdzanie dostępności sprzętu, wypożyczanie go i zwracanie. 


5. Użytkownicy systemu 

Użytkownik / rola 

Do czego będzie używał systemu? 

Klient: Sprawdza sprzęt i robi wypożyczenie
Pracownik: Obsługuje wypożyczenia i zwroty 
Administrator: Zarządza użytkownikami i sprzętem 


6. Interesariusze 

Interesariusz 
Dlaczego system jest dla niego istotny? 

Klient: Może łatwiej wypożyczyć sprzęt 

Pracownik: Łatwiej obsługuje wypożyczenia 

Właściciel: Może sprawdzić jaki sprzęt jest wypożyczony 

Administrator: Zarządza systemem 

 
7. Zakres IN 

Co system będzie realizował? 

1. Dodawanie sprzętu. 
2. Usuwanie sprzętu. 
3. Edycja sprzętu. 
4. Sprawdzanie dostępności sprzętu. 
5. Wypożyczanie sprzętu. 
6. Zwracanie sprzętu. 
7. Rejestracja użytkowników. 
8. Logowanie. 
9. Sprawdzanie historii wypożyczeń. 

 
8. Zakres OUT 

Czego system nie będzie realizował? 

1. Sprzedaży sprzętu. 
2. Naprawy sprzętu. 
3. Zamawiania sprzętu od producenta. 
4. Organizowania zawodów sportowych. 
5. Księgowości wypożyczalni. 

 

9. Najważniejsze funkcje 

1. Rejestracja użytkownika. 
2. Logowanie. 
3. Wyświetlanie sprzętu. 
4. Sprawdzanie dostępności. 
5. Wypożyczenie sprzętu. 
6. Zwrot sprzętu. 
7. Dodawanie sprzętu przez pracownika. 
8. Edycja sprzętu.
9. Historia wypożyczeń. 

 

10. Główne obiekty / dane 

1. Użytkownik. 
2. Sprzęt. 
3. Wypożyczenie. 
4. Zwrot. 
5. Kategoria sprzętu. 

 

11. Główne założenia 

◉ Każdy użytkownik ma konto. 

◉ Każdy sprzęt ma swój numer. 

◉ Sprzęt może być dostępny albo wypożyczony. 

◉ Nie można wypożyczyć sprzętu, który jest już wypożyczony. 

◉ Pracownik może dodawać i usuwać sprzęt. 

◉ Klient może sprawdzić dostępny sprzęt. 

◉ Po zwrocie sprzęt znowu może być dostępny. 

 

 

 

 

12. Wstępne ryzyka 

Ryzyko                     Dlaczego może być problemem? 

Za dużo funkcji      -      Możemy nie zdążyć zrobić wszystkiego 

Problemy z bazą danych  -   Mogą wystąpić błędy w danych 

Problemy z dostępnością  -  Ten sam sprzęt może zostać wypożyczony dwa razy 

 

13. Wstępnie rozważane technologie 

Frontend:  HTML, CSS, JavaScript 
Backend: Java Spring Boot 
Baza danych: PostgreSQL 
Inne: GitHub 
