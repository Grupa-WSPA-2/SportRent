# Wywiad 1 — SportRent

**Projekt:** System wypożyczalni sprzętu sportowego  
**Wersja dokumentu:** 0.1  
**Data:** do uzupełnienia  
**Czas trwania:** 15 minut  
**Forma:** Wywiad krzyżowy — zajęcia 3

---

## 1. Uczestnicy

- **Nazar Ostapenko** — koordynator projektu.
- **Bohdan Poderiako** — baza danych i analiza wymagań.
- **Kyrylo Skliarov** — backend.
- **Andriy Rushchak** — frontend i UI.
- **Rostyslav Svistelnytskyi** — testowanie.
- **Przedstawiciel wypożyczalni** — klient.

> Uwaga: role uczestników wywiadu należy potwierdzić po rozmowie.

---

## 2. Cel wywiadu

Celem wywiadu jest poznanie potrzeb klientów i pracowników wypożyczalni sprzętu sportowego oraz ustalenie zasad działania systemu SportRent.

Podczas rozmowy chcemy ustalić:

- jakie rodzaje sprzętu będą dostępne w systemie;
- jak klienci będą sprawdzać dostępność sprzętu;
- jak będzie przebiegał proces wypożyczania i zwracania sprzętu;
- jakie uprawnienia będą mieli pracownicy i administrator;
- jak system powinien obsługiwać opóźnienia, uszkodzenia i zagubienia sprzętu.

---

## 3. Ustalenia

### U-01. Dostępność sprzętu

System powinien umożliwiać sprawdzanie, czy dany sprzęt jest dostępny do wypożyczenia.

**Status:** Do potwierdzenia.

### U-02. Obsługa wypożyczeń

Pracownik powinien mieć możliwość rejestrowania wypożyczeń i zwrotów sprzętu.

**Status:** Do potwierdzenia.

### U-03. Zarządzanie sprzętem

Administrator powinien mieć możliwość dodawania i edytowania informacji o sprzęcie.

**Status:** Do potwierdzenia.

### U-04. Termin zwrotu

System powinien przechowywać datę wypożyczenia oraz planowany termin zwrotu.

**Status:** Do potwierdzenia.

### U-05. Dane klientów

System powinien przechowywać informacje potrzebne do obsługi klientów i ich wypożyczeń.

**Status:** Do potwierdzenia.

### U-06. Uszkodzony sprzęt

Należy ustalić, jak pracownik powinien postępować w przypadku zwrotu uszkodzonego sprzętu.

**Status:** Wymaga ustalenia.

---

## 4. Cytaty klienta

Poniższe wypowiedzi są przykładami i należy zastąpić je rzeczywistymi cytatami z przeprowadzonego wywiadu.

1. > „Chciałbym wiedzieć, jaki sprzęt jest dostępny przed przyjściem do wypożyczalni”.

2. > „Pracownik powinien szybko sprawdzić, kto wypożyczył dany sprzęt i kiedy ma go zwrócić”.

3. > „Dobrze byłoby otrzymywać przypomnienie o zbliżającym się terminie zwrotu”.

---

## 5. Nowe terminy do słownika

### 1. Wypożyczenie

Przekazanie sprzętu klientowi na określony czas.

### 2. Zwrot sprzętu

Oddanie wcześniej wypożyczonego sprzętu do wypożyczalni.

### 3. Dostępność sprzętu

Informacja określająca, czy dany egzemplarz sprzętu można aktualnie wypożyczyć.

### 4. Rezerwacja

Zgłoszenie chęci wypożyczenia sprzętu w określonym terminie.

### 5. Termin zwrotu

Ustalona data, do której klient powinien oddać wypożyczony sprzęt.

---

## 6. Zauważone problemy i sprzeczności

### Problem 1. Dostępność sprzętu

Sprzęt może znajdować się w wypożyczalni, ale być już wypożyczony. Należy ustalić, w jaki sposób system będzie określał jego dostępność.

### Problem 2. Rezerwacja i wypożyczenie

Rezerwacja nie oznacza, że klient odebrał już sprzęt. Należy ustalić, czy system będzie obsługiwał oba procesy.

### Problem 3. Uszkodzony sprzęt

Sprzęt może zostać zwrócony w złym stanie i nie nadawać się do kolejnego wypożyczenia. Trzeba ustalić sposób rejestrowania uszkodzeń.

---

## 7. Otwarte pytania

### Q-01

**Pytanie:** Czy klient musi posiadać konto, aby wypożyczyć sprzęt?

**Właściciel:** Nazar Ostapenko  
**Status:** Otwarte

### Q-02

**Pytanie:** Czy system powinien automatycznie naliczać opłaty za opóźniony zwrot?

**Właściciel:** Bohdan Poderiako  
**Status:** Otwarte

### Q-03

**Pytanie:** Czy klient powinien móc samodzielnie rezerwować sprzęt przez system?

**Właściciel:** Kyrylo Skliarov  
**Status:** Otwarte

### Q-04

**Pytanie:** Jak należy postępować w przypadku zagubienia lub uszkodzenia sprzętu?

**Właściciel:** Rostyslav Svistelnytskyi  
**Status:** Otwarte

### Q-05

**Pytanie:** Czy system powinien wysyłać przypomnienia o terminie zwrotu?

**Właściciel:** Andriy Rushchak  
**Status:** Otwarte

---

## 8. Wnioski zespołu

1. System SportRent powinien ułatwiać sprawdzanie dostępności sprzętu sportowego.
2. Ważną funkcją systemu będzie obsługa wypożyczeń i zwrotów.
3. Należy określić uprawnienia klientów, pracowników i administratora.
4. Trzeba ustalić zasady obsługi opóźnionych zwrotów, uszkodzeń i rezerwacji.
5. Zebrane informacje należy wykorzystać do uzupełnienia słownika dziedzinowego i wymagań systemu.

---

## 9. Dalsze działania

- [ ] Uzupełnić dokument o rzeczywiste odpowiedzi klienta.
- [ ] Zastąpić przykładowe cytaty prawdziwymi wypowiedziami.
- [ ] Zaktualizować słownik w pliku `docs/02-slownik.md`.
- [ ] Uzupełnić potrzeby w pliku `docs/03-wymagania.md`.
- [ ] Utworzyć Issues dla nierozstrzygniętych pytań.
- [ ] Przypisać każde zadanie do konkretnego członka zespołu.

---

**Status dokumentu:** Wersja robocza — do uzupełnienia po przeprowadzeniu wywiadu.
