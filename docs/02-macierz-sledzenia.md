# Macierz śledzenia wymagań — SportRent

**Wersja:** 0.2

## 1. Cel macierzy

Macierz śledzenia przedstawia powiązania pomiędzy potrzebami klienta, wymaganiami systemowymi, historyjkami użytkownika oraz procesami biznesowymi TO-BE.

Jej celem jest zapewnienie, że każda potrzeba klienta znajduje odzwierciedlenie w wymaganiach systemu, a wymagania funkcjonalne są powiązane z odpowiednimi krokami procesów.

Macierz umożliwia również sprawdzenie kompletności dokumentacji oraz śledzenie zmian w wymaganiach podczas rozwoju systemu.

## 2. Macierz śledzenia wymagań funkcjonalnych

| Potrzeba | Wymaganie | Historyjka | MoSCoW | Proces (krok TO-BE) |
|---|---|---|---|---|
| N-01 | FR-01 | US-01 | Must | P-01.1, P-01.2 |
| N-01 | FR-02 | — | Should | P-01.1, P-01.2 |
| N-02 | FR-03 | US-02 | Must | P-01.3, P-01.4 |
| N-02 | FR-04 | — | Should | P-01.3, P-01.4 |
| N-03 | FR-05 | US-03 | Must | — (zarządzanie katalogiem sprzętu) |
| N-03 | FR-06 | US-04 | Must | — (zarządzanie katalogiem sprzętu) |
| N-01, N-03 | FR-07 | US-05 | Must | P-01.8, P-02.6 |
| N-04 | FR-08 | US-06 | Must | P-01.6, P-01.7 |
| N-04 | FR-09 | US-07 | Must | P-01.7 |
| N-06 | FR-10 | US-07 | Must | P-01.7 |
| N-05 | FR-11 | US-08 | Must | P-02.5, P-02.6 |
| N-01, N-05 | FR-12 | US-09 | Must | P-02.6 |
| N-07 | FR-13 | US-10 | Must | P-02.4 |
| N-08 | FR-14 | — | Should | — (przegląd historii wypożyczeń) |
| N-04, N-06 | FR-15 | US-11 | Must | P-01.7, P-02.2 |

**Uwaga:** Znak „—” w kolumnie „Historyjka” oznacza, że wymaganie nie ma jeszcze osobnej historyjki użytkownika. Znak „—” w kolumnie „Proces” oznacza, że funkcjonalność nie została jeszcze przypisana do konkretnego kroku procesu TO-BE i wymaga sprawdzenia przez zespół.

## 3. Macierz śledzenia wymagań niefunkcjonalnych

| Potrzeba | Wymaganie | Historyjka | Proces |
|---|---|---|---|
| N-09 | NFR-01 | — | — (jakość i użyteczność interfejsu) |
| N-09 | NFR-02 | — | — (wydajność systemu) |
| N-10 | NFR-03 | — | — (kontrola dostępu) |
| N-10 | NFR-04 | — | — (ochrona danych użytkowników) |
| N-10 | NFR-05 | — | — (walidacja danych) |
| N-09 | NFR-06 | — | — (kompatybilność interfejsu) |
| N-09 | NFR-07 | — | — (utrzymanie i rozwój systemu) |
| N-10 | NFR-08 | — | — (tworzenie kopii zapasowych) |

Wymagania niefunkcjonalne opisują jakość i ograniczenia systemu, dlatego nie muszą odpowiadać pojedynczemu krokowi procesu biznesowego.

## 4. Powiązanie reguł biznesowych

| Reguła | Powiązane wymagania |
|---|---|
| BR-01 | FR-07, FR-08 |
| BR-02 | FR-05, FR-06 |
| BR-03 | FR-08 |
| BR-04 | FR-09, FR-10 |
| BR-05 | FR-11, FR-12 |
| BR-06 | FR-07, FR-13 |
| BR-07 | FR-08, FR-14 |

## 5. Zasady aktualizacji macierzy

1. Każda potrzeba klienta powinna być powiązana z co najmniej jednym wymaganiem systemowym.
2. Każde wymaganie funkcjonalne powinno być powiązane z odpowiednią potrzebą klienta.
3. Wymagania funkcjonalne powinny być powiązane z historyjkami użytkownika, jeśli dotyczą funkcjonalności opisanej z perspektywy użytkownika.
4. Każde wymaganie funkcjonalne powinno mieć przypisany krok procesu TO-BE albo uzasadnienie braku takiego kroku.
5. Priorytety MoSCoW powinny być zgodne z dokumentem `03-wymagania.md`.
6. Każda zmiana wymagania powinna być odzwierciedlona w macierzy.
7. Wątpliwości dotyczące powiązań należy zapisywać jako Issues w repozytorium projektu.

## 6. Podsumowanie

Macierz łączy potrzeby klienta, wymagania funkcjonalne i niefunkcjonalne, historyjki użytkownika oraz reguły biznesowe.

Umożliwia sprawdzenie, czy wymagania wynikają z potrzeb klienta i czy zostały uwzględnione w procesach biznesowych TO-BE.

Macierz będzie aktualizowana wraz z rozwojem dokumentacji i doprecyzowaniem procesów systemu SportRent.
