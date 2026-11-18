# Wymagania systemu SportRent

Wersja: 0.3

## 1. Lista potrzeb klienta

| ID | Potrzeba | Źródło |
|---|---|---|
| N-01 | Klient potrzebuje sprawdzać dostępność sprzętu sportowego. | Wywiad 1 |
| N-02 | Klient potrzebuje przeglądać informacje o sprzęcie i jego cenie. | Wywiad 1 |
| N-03 | Pracownik potrzebuje dodawać i aktualizować sprzęt. | Wywiad 1 |
| N-04 | Pracownik potrzebuje rejestrować wypożyczenia. | Wywiad 1 |
| N-05 | Pracownik potrzebuje rejestrować zwroty sprzętu. | Wywiad 1 |
| N-06 | Pracownik potrzebuje kontrolować terminy zwrotów. | Wywiad 1 |
| N-07 | Pracownik potrzebuje zapisywać informacje o uszkodzeniach sprzętu. | Wywiad 1 |
| N-08 | Pracownik potrzebuje przeglądać historię wypożyczeń. | Wywiad 1 |
| N-09 | Użytkownik potrzebuje łatwego i zrozumiałego interfejsu. | Założenie zespołu |
| N-10 | Użytkownik potrzebuje ochrony swoich danych. | Założenie zespołu |

## 2. Wymagania funkcjonalne (FR)

Priorytety według metody MoSCoW:

- Must – wymaganie niezbędne do działania podstawowej wersji systemu.
- Should – ważne wymaganie, ale system może działać bez niego.
- Could – dodatkowa funkcjonalność, którą można zrealizować, jeśli wystarczy czasu.
- Won't – funkcjonalność wyłączona z aktualnej wersji projektu.

| ID | Wymaganie | Potrzeba | Priorytet |
|---|---|---|---|
| FR-01 | System powinien wyświetlać listę dostępnego sprzętu sportowego. | N-01 | Must |
| FR-02 | System powinien umożliwiać wyszukiwanie sprzętu według nazwy. | N-01 | Should |
| FR-03 | System powinien wyświetlać szczegółowe informacje o wybranym sprzęcie. | N-02 | Must |
| FR-04 | System powinien wyświetlać cenę wypożyczenia, jeśli została określona. | N-02 | Should |
| FR-05 | System powinien umożliwiać pracownikowi dodawanie nowego sprzętu. | N-03 | Must |
| FR-06 | System powinien umożliwiać pracownikowi edycję danych sprzętu. | N-03 | Must |
| FR-07 | System powinien umożliwiać pracownikowi zmianę statusu sprzętu. | N-01, N-03 | Must |
| FR-08 | System powinien umożliwiać pracownikowi rejestrowanie wypożyczenia sprzętu. | N-04 | Must |
| FR-09 | System powinien zapisywać datę rozpoczęcia wypożyczenia. | N-04 | Must |
| FR-10 | System powinien zapisywać planowany termin zwrotu sprzętu. | N-06 | Must |
| FR-11 | System powinien umożliwiać pracownikowi rejestrowanie zwrotu sprzętu. | N-05 | Must |
| FR-12 | System powinien aktualizować status dostępności sprzętu po jego zwrocie. | N-01, N-05 | Must |
| FR-13 | System powinien umożliwiać pracownikowi zapisanie informacji o uszkodzeniu sprzętu. | N-07 | Must |
| FR-14 | System powinien umożliwiać przeglądanie historii wypożyczeń. | N-08 | Should |
| FR-15 | System powinien umożliwiać pracownikowi przeglądanie aktualnych wypożyczeń wraz z terminami zwrotu. | N-04, N-06 | Must |

## 3. Wymagania niefunkcjonalne (NFR)

Kategorie oparte na modelu jakości ISO/IEC 25010.
| ID | Wymaganie | Potrzeba | Kategoria ISO/IEC 25010 |
|---|---|---|---|
| NFR-01 | Nowy użytkownik powinien być w stanie wykonać podstawowe czynności w systemie bez korzystania z instrukcji. | N-09 | Użyteczność (Usability) |
| NFR-02 | Wynik podstawowej operacji, takiej jak wyświetlenie listy sprzętu, powinien pojawić się w czasie nie dłuższym niż 3 sekundy w normalnych warunkach pracy. | N-09 | Efektywność działania (Performance Efficiency) |
| NFR-03 | System powinien ograniczać dostęp do funkcji pracownika osobom bez odpowiednich uprawnień. | N-10 | Bezpieczeństwo (Security) |
| NFR-04 | Dane użytkowników powinny być dostępne wyłącznie dla osób posiadających odpowiednie uprawnienia. | N-10 | Bezpieczeństwo (Security) |
| NFR-05 | System powinien sprawdzać poprawność wymaganych danych przed ich zapisaniem i informować o błędach. | N-10 | Niezawodność (Reliability) |
| NFR-06 | Interfejs powinien poprawnie wyświetlać się na ekranach komputerów i telefonów w aktualnych wersjach popularnych przeglądarek. | N-09 | Kompatybilność (Compatibility) |
| NFR-07 | Kod źródłowy i dokumentacja powinny być uporządkowane oraz podzielone na moduły, aby ułatwić dalszy rozwój systemu. | N-09 | Łatwość utrzymania (Maintainability) |
| NFR-08 | System powinien umożliwiać tworzenie kopii zapasowych danych oraz ich odtworzenie w przypadku awarii. | N-10 | Niezawodność (Reliability) |

## 4. Reguły biznesowe (BR)

Reguły biznesowe określają zasady działania wypożyczalni niezależnie od sposobu implementacji systemu.

| ID | Reguła biznesowa | Powiązane wymagania |
|---|---|---|
| BR-01 | Sprzęt, który jest już wypożyczony, nie może zostać ponownie wypożyczony. | FR-07, FR-08 |
| BR-02 | Każdy egzemplarz sprzętu musi posiadać unikalny identyfikator. | FR-05, FR-06 |
| BR-03 | Wypożyczenie sprzętu może zostać zarejestrowane wyłącznie dla istniejącego klienta. | FR-08 |
| BR-04 | Każde wypożyczenie musi posiadać datę rozpoczęcia oraz planowany termin zwrotu. | FR-09, FR-10 |
| BR-05 | Po zarejestrowaniu zwrotu system powinien zaktualizować status sprzętu. | FR-11, FR-12 |
| BR-06 | Uszkodzony sprzęt nie może otrzymać statusu „Dostępny”, dopóki nie zostanie uznany za sprawny przez pracownika. | FR-07, FR-13 |
| BR-07 | Każde wypożyczenie musi być powiązane z konkretnym klientem i konkretnym egzemplarzem sprzętu. | FR-08, FR-14 |

## 5. Historyjki użytkownika (User Stories)

Historyjki użytkownika opisują funkcjonalności z perspektywy osób korzystających z systemu.

| ID | Historyjka | Powiązane wymaganie | Priorytet |
|---|---|---|---|
| US-01 | Jako klient chcę przeglądać listę dostępnego sprzętu, aby wiedzieć, co mogę wypożyczyć. | FR-01 | Must |
| US-02 | Jako klient chcę zobaczyć szczegóły sprzętu, aby poznać jego właściwości przed wypożyczeniem. | FR-03 | Must |
| US-03 | Jako pracownik chcę dodawać nowy sprzęt, aby aktualizować ofertę wypożyczalni. | FR-05 | Must |
| US-04 | Jako pracownik chcę edytować dane sprzętu, aby informacje w systemie były aktualne. | FR-06 | Must |
| US-05 | Jako pracownik chcę zmieniać status sprzętu, aby prawidłowo określać jego dostępność. | FR-07 | Must |
| US-06 | Jako pracownik chcę rejestrować wypożyczenie, aby system przechowywał informacje o wydanym sprzęcie. | FR-08 | Must |
| US-07 | Jako pracownik chcę zapisywać datę rozpoczęcia i planowany termin zwrotu, aby kontrolować czas wypożyczenia. | FR-09, FR-10 | Must |
| US-08 | Jako pracownik chcę rejestrować zwrot sprzętu, aby aktualizować informacje o wypożyczeniu. | FR-11 | Must |
| US-09 | Jako pracownik chcę, aby status sprzętu aktualizował się po zwrocie, aby jego dostępność była prawidłowa. | FR-12 | Must |
| US-10 | Jako pracownik chcę zapisywać informacje o uszkodzeniach, aby uszkodzony sprzęt nie był ponownie wypożyczany. | FR-13 | Must |
| US-11 | Jako pracownik chcę przeglądać aktualne wypożyczenia i terminy zwrotów, aby kontrolować wypożyczony sprzęt. | FR-15 | Must |

### 5.1. Kryteria akceptacji — Given / When / Then
Kryteria akceptacji określają warunki, które muszą zostać spełnione, aby uznać daną funkcjonalność za poprawnie działającą.

US-01 — Przeglądanie dostępnego sprzętu

- Given: Użytkownik otworzył listę sprzętu.
- When: System pobiera dostępne egzemplarze.
- Then: System wyświetla listę sprzętu, którego status to „Dostępny”.

US-02 — Szczegóły sprzętu

- Given: Użytkownik widzi listę sprzętu.
- When: Wybiera konkretny egzemplarz.
- Then: System wyświetla jego nazwę, kategorię, opis i aktualny status.

US-03 — Dodawanie sprzętu

- Given: Pracownik jest zalogowany i posiada odpowiednie uprawnienia.
- When: Wprowadza poprawne dane nowego sprzętu i zapisuje formularz.
- Then: System zapisuje sprzęt i nadaje mu unikalny identyfikator.

US-04 — Edycja danych sprzętu

- Given: Sprzęt istnieje w systemie.
- When: Uprawniony pracownik zmienia jego dane i zapisuje zmiany.
- Then: System zapisuje zaktualizowane informacje.

US-05 — Zmiana statusu sprzętu

- Given: Pracownik wybrał istniejący egzemplarz sprzętu.
- When: Zmienia jego status na dozwolony status.
- Then: System zapisuje nowy status i aktualizuje informację o dostępności.

US-06 — Rejestrowanie wypożyczenia

- Given: Klient istnieje w systemie, a wybrany sprzęt ma status „Dostępny”.
- When: Pracownik rejestruje wypożyczenie.
- Then: System zapisuje wypożyczenie i zmienia status sprzętu na „Wypożyczony”.

US-07 — Zapisywanie dat wypożyczenia

- Given: Pracownik rejestruje nowe wypożyczenie.
- When: Wprowadza datę rozpoczęcia i planowany termin zwrotu.
- Then: System zapisuje obie daty przy danym wypożyczeniu.

US-08 — Rejestrowanie zwrotu

- Given: Istnieje aktywne wypożyczenie sprzętu.
- When: Pracownik rejestruje zwrot.
- Then: System zapisuje informację o zwrocie i aktualizuje status wypożyczenia.

US-09 — Aktualizacja dostępności po zwrocie

- Given: Pracownik zarejestrował zwrot sprzętu, który nie jest uszkodzony.
- When: System przetwarza zwrot.
- Then: Status sprzętu zostaje zmieniony na „Dostępny”.

US-10 — Zapisywanie uszkodzeń

- Given: Pracownik stwierdził uszkodzenie zwróconego sprzętu.
- When: Wprowadza informację o uszkodzeniu.
- Then: System zapisuje informację, a sprzęt nie jest oznaczany jako dostępny.

US-11 — Przegląd aktualnych wypożyczeń

- Given: W systemie znajdują się zarejestrowane wypożyczenia.
- When: Pracownik otwiera listę aktualnych wypożyczeń.
- Then: System wyświetla aktywne wypożyczenia wraz z klientem, sprzętem i planowanym terminem zwrotu.

## 6. Uwagi i założenia

1. Lista potrzeb i wymagań jest wstępna i powinna zostać zweryfikowana na podstawie wywiadu z klientem oraz decyzji zespołu.
2. Reguły biznesowe BR-01–BR-07 są propozycjami zespołu i wymagają potwierdzenia.
3. Wymaganie NFR-02 zawiera proponowany limit 3 sekund. Warunki testowania i obciążenie systemu powinny zostać doprecyzowane.
4. Wymagania dotyczące rezerwacji sprzętu z wyprzedzeniem, płatności, kaucji i automatycznych powiadomień nie zostały uwzględnione, ponieważ wymagają dodatkowego potwierdzenia.
5. Priorytety MoSCoW mogą zostać zmienione po konsultacji z klientem i analizie procesów AS-IS / TO-BE.
6. Kryteria Given/When/Then dotyczą wszystkich historyjek oznaczonych jako Must.

   
