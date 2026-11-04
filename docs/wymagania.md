# Wymagania systemu SportRent

**Wersja:** 0.2

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


## 2. Wymagania biznesowe (BR)

| ID | Wymaganie biznesowe | Cel |
|---|---|---|
| BR-01 | System powinien usprawnić proces wypożyczania sprzętu sportowego. | Skrócenie czasu obsługi klienta. |
| BR-02 | System powinien centralizować informacje o sprzęcie sportowym. | Ułatwienie zarządzania sprzętem. |
| BR-03 | System powinien poprawić kontrolę dostępności sprzętu. | Ograniczenie pomyłek przy wypożyczeniach. |
| BR-04 | System powinien umożliwiać prowadzenie historii wypożyczeń i zwrotów. | Ułatwienie kontroli operacji. |
| BR-05 | System powinien ograniczyć błędy związane z ręcznym zapisywaniem danych. | Poprawa dokładności informacji. |

## 3. Wymagania funkcjonalne (FR)

| ID | Wymaganie | Potrzeba | Priorytet (MoSCoW) |
|---|---|---|---|
| FR-01 | System powinien wyświetlać listę dostępnego sprzętu. | N-01 | Must |
| FR-02 | System powinien umożliwiać wyszukiwanie sprzętu według nazwy. | N-01 | Should |
| FR-03 | System powinien wyświetlać szczegóły wybranego sprzętu. | N-02 | Must |
| FR-04 | System powinien wyświetlać cenę wypożyczenia, jeśli została określona. | N-02 | Must |
| FR-05 | System powinien umożliwiać pracownikowi dodawanie sprzętu. | N-03 | Must |
| FR-06 | System powinien umożliwiać pracownikowi edycję danych sprzętu. | N-03 | Must |
| FR-07 | System powinien umożliwiać zmianę statusu sprzętu. | N-01, N-03 | Must |
| FR-08 | System powinien umożliwiać pracownikowi rejestrowanie wypożyczenia. | N-04 | Must |
| FR-09 | System powinien zapisywać datę rozpoczęcia wypożyczenia. | N-04 | Must |
| FR-10 | System powinien zapisywać planowany termin zwrotu. | N-06 | Must |
| FR-11 | System powinien umożliwiać rejestrowanie zwrotu sprzętu. | N-05 | Must |
| FR-12 | System powinien aktualizować dostępność sprzętu po jego zwrocie. | N-01, N-05 | Must |
| FR-13 | System powinien umożliwiać zapisanie informacji o uszkodzeniu sprzętu. | N-07 | Should |
| FR-14 | System powinien umożliwiać przeglądanie historii wypożyczeń. | N-08 | Should |
| FR-15 | System powinien umożliwiać pracownikowi przeglądanie aktualnych wypożyczeń. | N-04, N-06 | Must |

## 4. Wymagania niefunkcjonalne (NFR)

| ID | Wymaganie | Potrzeba | Charakterystyka ISO/IEC 25010 |
|---|---|---|---|
| NFR-01 | Interfejs powinien być zrozumiały dla nowego użytkownika bez specjalnego szkolenia. | N-09 | Zdolność do interakcji |
| NFR-02 | Podstawowe operacje powinny wyświetlać wynik w czasie nie dłuższym niż 3 sekundy w normalnych warunkach pracy. | N-09 | Efektywność działania |
| NFR-03 | System powinien ograniczać dostęp do funkcji pracownika osobom bez odpowiednich uprawnień. | N-10 | Bezpieczeństwo |
| NFR-04 | Dane użytkowników powinny być dostępne tylko dla uprawnionych osób. | N-10 | Bezpieczeństwo |
| NFR-05 | System powinien sprawdzać poprawność wymaganych danych przed ich zapisaniem. | N-10 | Adekwatność funkcjonalna |
| NFR-06 | Interfejs powinien poprawnie wyświetlać się na ekranach komputerów i telefonów. | N-09 | Elastyczność |
| NFR-07 | Kod i dokumentacja powinny być uporządkowane, aby ułatwić dalszy rozwój systemu. | N-09 | Łatwość utrzymania |
| NFR-08 | System powinien umożliwiać regularne tworzenie kopii zapasowych danych. | N-10 | Niezawodność |

## 5. Uwagi

Lista potrzeb i wymagań jest wstępna. Należy ją zweryfikować na podstawie wywiadu z klientem oraz decyzji prowadzącego.

Wymagania dotyczące rezerwacji, płatności, kaucji i automatycznych powiadomień nie zostały uwzględnione, ponieważ wymagają dodatkowego potwierdzenia.
