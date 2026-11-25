# Szczegółowe scenariusze przypadków użycia

---

<a name="pu-01"></a>
## PU-01: Przeglądanie katalogu i sprawdzanie dostępności sprzętu

* **Aktor główny:** Klient (niezalogowany lub zalogowany)
* **Aktorzy pomocniczy:** Brak
* **Cel:** Wyszukanie odpowiedniego sprzętu sportowego oraz sprawdzenie jego dostępności w wybranym terminie.
* **Warunki początkowe:** System jest dostępny online; w bazie znajduje się co najmniej jeden aktywny przedmiot.
* **Warunki końcowe:** Klient widzi listę dostępnego sprzętu wraz z ceną za dobę i wysokością kaucji.

**Scenariusz główny:**
1. Klient otwiera stronę główną lub zakładkę „Katalog sprzętu”.
2. Klient wybiera kategorię (np. narty, rowery, sprzęt wodny) oraz filtruje wyniki po rozmiarze lub parametrach technicznych.
3. Klient wskazuje planowaną datę odbioru oraz datę zwrotu sprzętu.
4. System sprawdza stany magazynowe oraz istniejące rezerwacje w podanym przedziale czasowym.
5. System wyświetla listę dostępnych egzemplarzy wraz ze zdjęciem, opisem technicznym, stawką dobową oraz kwotą kaucji.

**Scenariusze alternatywne:**
* **4a. Brak dostępnego sprzętu w wybranym terminie:**
  1. System wyświetla komunikat o braku dostępności dla wybranych dat.
  2. System proponuje najbliższe wolne terminy lub podobny sprzęt z tej samej kategorii.

---

<a name="pu-02"></a>
## PU-02: Rezerwacja sprzętu sportowego online

* **Aktor główny:** Klient (zalogowany)
* **Aktorzy pomocniczy:** System płatności online
* **Cel:** Zarezerwowanie wybranego sprzętu na określony termin.
* **Warunki początkowe:** Klient jest zalogowany w systemie i wybrał dostępny sprzęt (PU-01).
* **Warunki końcowe:** Rezerwacja otrzymuje status „Potwierdzona”, a wybrane egzemplarze zostają zablokowane w kalendarzu.

**Scenariusz główny:**
1. Klient klika przycisk „Rezerwuj” przy wybranym sprzęcie.
2. System wyświetla podsumowanie rezerwacji: daty, liczbę dni, koszt wypożyczenia oraz kwotę kaucji zwrotnej.
3. Klient akceptuje regulamin wypożyczalni i potwierdza chęć złożenia rezerwacji.
4. System tworzy wstępną rezerwację ze statusem „Oczekuje na płatność” i blokuje sprzęt na 15 minut.
5. System uruchamia przypadek użycia **PU-03 (Opłacenie rezerwacji i blokada kaucji)**.
6. Po otrzymaniu potwierdzenia płatności system zmienia status rezerwacji na „Potwierdzona” i wysyła klientowi kod odbioru (QR / numer rezerwacji).

**Scenariusze alternatywne:**
* **4a. Egzemplarz został w międzyczasie zarezerwowany przez innego użytkownika:**
  1. System przerywa proces i informuje o zmianie dostępności.
  2. Klient wraca do kroku wyboru innego egzemplarza (PU-01).
* **5a. Płatność nie powiodła się lub minął czas 15 minut:**
  1. System anuluje wstępną rezerwację i zwalnia blokadę sprzętu.

---

<a name="pu-03"></a>
## PU-03: Opłacenie rezerwacji i blokada kaucji

* **Aktor główny:** Klient
* **Aktorzy pomocniczy:** System płatności online (operator płatności)
* **Cel:** Bezpieczne opłacenie najmu oraz zabezpieczenie kaucji zwrotnej.
* **Warunki początkowe:** Istnieje rezerwacja ze statusem „Oczekuje na płatność”.
* **Warunki końcowe:** Opłata za najem zaksięgowana, kaucja zablokowana na karcie lub koncie klienta.

**Scenariusz główny:**
1. System przekierowuje klienta do bramki płatniczej z kwotą najmu i kaucji.
2. Klient wybiera metodę płatności (BLIK, karta płatnicza, szybki przelew) i autoryzuje transakcję.
3. Operator płatności weryfikuje środki i przesyła do systemu SportRent potwierdzenie autoryzacji.
4. System zapisuje identyfikator transakcji w historii rezerwacji.

**Scenariusze alternatywne:**
* **3a. Odrzucenie transakcji przez bank lub operatora:**
  1. Operator zwraca błąd płatności.
  2. System wyświetla komunikat o nieudanej płatności i umożliwia ponowną próbę w ramach limitu czasu rezerwacji.

---

<a name="pu-04"></a>
## PU-04: Wydanie sprzętu w punkcie wypożyczalni

* **Aktor główny:** Pracownik wypożyczalni
* **Aktorzy pomocniczy:** Klient
* **Cel:** Fizyczne przekazanie zarezerwowanego sprzętu klientowi i zmiana statusu wypożyczenia.
* **Warunki początkowe:** Klient posiada rezerwację o statusie „Potwierdzona” i stawił się w punkcie odbioru.
* **Warunki końcowe:** Sprzęt wydany klientowi, status rezerwacji zmieniony na „W trakcie realizacji”.

**Scenariusz główny:**
1. Klient podaje numer rezerwacji lub okazuje kod QR pracownikowi.
2. Pracownik wyszukuje rezerwację w panelu pracownika i weryfikuje tożsamość klienta.
3. Pracownik przygotowuje przypisane egzemplarze sprzętu i sprawdza ich stan techniczny w obecności klienta.
4. Pracownik zaznacza w systemie ewentualne istniejące drobne rysy lub uwagi w protokole wydania.
5. Pracownik klika „Potwierdź wydanie sprzętu”.
6. System zmienia status rezerwacji na „W trakcie realizacji” i rejestruje dokładną godzinę wydania.

**Scenariusze alternatywne:**
* **3a. Wykrycie usterki przygotowanego egzemplarza przed wydaniem:**
  1. Pracownik oznacza egzemplarz jako „W serwisie”.
  2. Pracownik przypisuje do rezerwacji inny dostępny egzemplarz tej samej klasy lub wyższej bez dopłaty dla klienta.

---

<a name="pu-05"></a>
## PU-05: Zwrot sprzętu, weryfikacja stanu i zwrot kaucji

* **Aktor główny:** Pracownik wypożyczalni
* **Aktorzy pomocniczy:** Klient, System płatności online
* **Cel:** Przyjęcie zwracanego sprzętu, ocena jego stanu oraz rozliczenie kaucji.
* **Warunki początkowe:** Rezerwacja ma status „W trakcie realizacji”, a klient zwraca sprzęt do punktu.
* **Warunki końcowe:** Rezerwacja zakończona, sprzęt wraca do puli dostępnych (lub trafia do serwisu), kaucja rozliczona.

**Scenariusz główny:**
1. Pracownik wyszukuje aktywną rezerwację po numerze lub danych klienta.
2. Pracownik przyjmuje sprzęt i dokonuje oględzin technicznych (kompletność, brak uszkodzeń mechanicznych).
3. Pracownik potwierdza w systemie zwrot bez uszkodzeń oraz brak przekroczenia terminu zwrotu.
4. System zmienia status rezerwacji na „Zakończona” i przywraca dostępność egzemplarza w katalogu.
5. System automatycznie zleca operatorowi płatności zwolnienie pełnej kwoty kaucji dla klienta.

**Scenariusze alternatywne:**
* **2a. Stwierdzenie uszkodzenia lub braku elementu wyposażenia:**
  1. Pracownik odnotowuje uszkodzenie w protokole zwrotu i wybiera z cennika kwotę potrącenia z kaucji.
  2. System potrąca wskazaną kwotę z kaucji, zleca zwrot pozostałej części (jeśli dotyczy) oraz zmienia status egzemplarza na „Do naprawy”.
* **3a. Przekroczenie terminu zwrotu (opóźnienie):**
  1. System automatycznie nalicza dopłatę za dodatkowe godziny lub doby zgodnie z cennikiem.
  2. Dopłata jest rozliczana z kaucji lub opłacana na miejscu przez klienta.
