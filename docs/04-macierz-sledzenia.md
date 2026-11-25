# Macierz śledzenia wymagań — SportRent

**Projekt:** System wypożyczalni sprzętu sportowego  

## 1. Cel dokumentu

Celem macierzy śledzenia wymagań jest przedstawienie powiązań pomiędzy potrzebami użytkowników, wymaganiami systemowymi, historyjkami użytkownika oraz procesami biznesowymi.

Macierz umożliwia sprawdzenie, czy wszystkie wymagania zostały uwzględnione w projekcie SportRent i powiązane z odpowiednimi procesami.

## 2. Legenda procesów

| ID procesu | Nazwa procesu | Opis |
|---|---|---|
| P-01 | Wypożyczenie sprzętu | Proces sprawdzania dostępności i rejestrowania wypożyczenia sprzętu. |
| P-02 | Zwrot sprzętu | Proces przyjmowania zwracanego sprzętu i aktualizacji jego statusu. |
| P-03 | Zarządzanie sprzętem | Proces dodawania, edytowania i aktualizacji informacji o sprzęcie. |

## 3. Macierz śledzenia wymagań funkcjonalnych

| Potrzeba | Wymaganie | Historyjka użytkownika | MoSCoW | Proces | PU |
|---|---|---|---|---|---|
| N-01 | FR-01 | US-01 | Must | P-01 | PU-01 |
| N-01 | FR-02 | — | Should | P-01 | PU-01 |
| N-02 | FR-03 | US-02 | Must | P-01 | PU-01 |
| N-02 | FR-04 | — | Should | P-01 | PU-01 |
| N-03 | FR-05 | US-03 | Must | P-03 | PU-06 |
| N-03 | FR-06 | US-04 | Must | P-03 | PU-06 |
| N-01, N-03 | FR-07 | US-05 | Must | P-01, P-02, P-03 | PU-04, PU-05, PU-06 |
| N-04 | FR-08 | US-06 | Must | P-01 | PU-02, PU-04 |
| N-04 | FR-09 | US-07 | Must | P-01 | PU-02, PU-04 |
| N-06 | FR-10 | US-07 | Must | P-01 | PU-02, PU-04 |
| N-05 | FR-11 | US-08 | Must | P-02 | PU-05 |
| N-01, N-05 | FR-12 | US-09 | Must | P-02 | PU-05 |
| N-07 | FR-13 | US-10 | Must | P-02 | PU-05 |
| N-08 | FR-14 | — | Should | P-02 | PU-05 |
| N-04, N-06 | FR-15 | US-11 | Must | P-01, P-02 | PU-04, PU-05 |

## 4. Macierz śledzenia wymagań niefunkcjonalnych

| Potrzeba | Wymaganie | Kategoria ISO/IEC 25010 | MoSCoW |
|---|---|---|---|
| N-09 | NFR-01 | Użyteczność (Usability) | Must |
| N-09 | NFR-02 | Wydajność (Performance Efficiency) | Should |
| N-10 | NFR-03 | Bezpieczeństwo (Security) | Must |
| N-10 | NFR-04 | Bezpieczeństwo (Security) | Must |
| N-10 | NFR-05 | Niezawodność (Reliability) | Must |
| N-09 | NFR-06 | Elastyczność (Flexibility) | Should |
| N-09 | NFR-07 | Łatwość utrzymania (Maintainability) | Should |
| N-10 | NFR-08 | Niezawodność (Reliability) | Should |

Wymagania niefunkcjonalne dotyczą jakości i sposobu działania całego systemu, dlatego nie są przypisane do pojedynczego procesu biznesowego.

## 5. Powiązania reguł biznesowych

| Reguła biznesowa | Powiązane wymagania |
|---|---|
| BR-01 | FR-07, FR-08 |
| BR-02 | FR-05, FR-06 |
| BR-03 | FR-08 |
| BR-04 | FR-09, FR-10 |
| BR-05 | FR-11, FR-12 |
| BR-06 | FR-07, FR-13 |
| BR-07 | FR-08, FR-14 |

## 6. Powiązania historyjek użytkownika

| ID | Historyjka użytkownika | Powiązane wymagania |
|---|---|---|
| US-01 | Jako klient chcę przeglądać dostępny sprzęt, aby wybrać interesujący mnie produkt. | FR-01 |
| US-02 | Jako klient chcę zobaczyć szczegółowe informacje o sprzęcie, aby poznać jego właściwości. | FR-03 |
| US-03 | Jako pracownik chcę dodawać nowy sprzęt, aby aktualizować ofertę wypożyczalni. | FR-05 |
| US-04 | Jako pracownik chcę edytować dane sprzętu, aby utrzymywać aktualne informacje. | FR-06 |
| US-05 | Jako pracownik chcę zmieniać status sprzętu, aby kontrolować jego dostępność. | FR-07 |
| US-06 | Jako pracownik chcę rejestrować wypożyczenia, aby zapisywać informacje o wynajmie sprzętu. | FR-08 |
| US-07 | Jako pracownik chcę zapisywać datę rozpoczęcia i planowaną datę zwrotu, aby kontrolować okres wypożyczenia. | FR-09, FR-10 |
| US-08 | Jako pracownik chcę rejestrować zwroty sprzętu, aby aktualizować informacje o wypożyczeniach. | FR-11 |
| US-09 | Jako pracownik chcę aktualizować dostępność sprzętu po jego zwrocie, aby inni klienci mogli go wypożyczyć. | FR-12 |
| US-10 | Jako pracownik chcę zapisywać informacje o uszkodzeniach sprzętu, aby kontrolować jego stan techniczny. | FR-13 |
| US-11 | Jako pracownik chcę przeglądać aktualne wypożyczenia i terminy zwrotu, aby kontrolować wypożyczony sprzęt. | FR-15 |

## 7. Podsumowanie

Macierz śledzenia wymagań przedstawia powiązania pomiędzy potrzebami użytkowników, wymaganiami funkcjonalnymi i niefunkcjonalnymi, regułami biznesowymi, historyjkami użytkownika, przypadkami użycia (PU) oraz procesami biznesowymi.

Dzięki macierzy możliwe jest sprawdzenie kompletności wymagań oraz kontrolowanie ich realizacji na kolejnych etapach projektu SportRent.

Powiązania z procesami P-01, P-02 i P-03 mają charakter wstępny i powinny zostać zweryfikowane po przygotowaniu oraz przeglądzie diagramów BPMN.
