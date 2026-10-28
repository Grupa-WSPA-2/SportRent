# Wymagania systemu SportRent

**Wersja:** 0.3

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

| ID | Wymaganie | Potrzeba |
|---|---|---|
| FR-01 | System powinien wyświetlać listę dostępnego sprzętu. | N-01 |
| FR-02 | System powinien umożliwiać wyszukiwanie sprzętu według nazwy. | N-01 |
| FR-03 | System powinien wyświetlać szczegóły wybranego sprzętu. | N-02 |
| FR-04 | System powinien wyświetlać cenę wypożyczenia, jeśli została określona. | N-02 |
| FR-05 | System powinien umożliwiać pracownikowi dodawanie sprzętu. | N-03 |
| FR-06 | System powinien umożliwiać pracownikowi edycję danych sprzętu. | N-03 |
| FR-07 | System powinien umożliwiać zmianę statusu sprzętu. | N-01, N-03 |
| FR-08 | System powinien umożliwiać pracownikowi rejestrowanie wypożyczenia. | N-04 |
| FR-09 | System powinien zapisywać datę rozpoczęcia wypożyczenia. | N-04 |
| FR-10 | System powinien zapisywać planowany termin zwrotu. | N-06 |
| FR-11 | System powinien umożliwiać rejestrowanie zwrotu sprzętu. | N-05 |
| FR-12 | System powinien aktualizować dostępność sprzętu po jego zwrocie. | N-01, N-05 |
| FR-13 | System powinien umożliwiać zapisanie informacji o uszkodzeniu sprzętu. | N-07 |
| FR-14 | System powinien umożliwiać przeglądanie historii wypożyczeń. | N-08 |
| FR-15 | System powinien umożliwiać pracownikowi przeglądanie aktualnych wypożyczeń. | N-04, N-06 |

## 3. Wymagania niefunkcjonalne (NFR)

| ID | Wymaganie | Potrzeba |
|---|---|---|
| NFR-01 | Interfejs powinien być zrozumiały dla nowego użytkownika bez specjalnego szkolenia. | N-09 |
| NFR-02 | Podstawowe operacje powinny wyświetlać wynik w czasie nie dłuższym niż 3 sekundy w normalnych warunkach pracy. | N-09 |
| NFR-03 | System powinien ograniczać dostęp do funkcji pracownika osobom bez odpowiednich uprawnień. | N-10 |
| NFR-04 | Dane użytkowników powinny być dostępne tylko dla uprawnionych osób. | N-10 |
| NFR-05 | System powinien sprawdzać poprawność wymaganych danych przed ich zapisaniem. | N-10 |
| NFR-06 | Interfejs powinien poprawnie wyświetlać się na ekranach komputerów i telefonów. | N-09 |
| NFR-07 | Kod i dokumentacja powinny być uporządkowane, aby ułatwić dalszy rozwój systemu. | N-09 |
| NFR-08 | System powinien umożliwiać regularne tworzenie kopii zapasowych danych. | N-10 |

## 4. Uwagi

Lista potrzeb i wymagań jest wstępna. Należy ją zweryfikować na podstawie wywiadu z klientem oraz decyzji prowadzącego.

Wymagania dotyczące rezerwacji, płatności, kaucji i automatycznych powiadomień nie zostały uwzględnione, ponieważ wymagają dodatkowego potwierdzenia.
