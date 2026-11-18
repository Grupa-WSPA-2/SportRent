# P-00: Wypożyczenie sprzętu i odzieży sportowej (AS-IS)

**Wersja:** 0.1 · **Właściciel:** @NzDDD;@Bohdan52;Andrusha0500;@rostik88afk

## Cel procesu
Obsługa wypożyczenia sprzętu lub odzieży sportowej klientowi w trybie stacjonarnym/telefonicznym przed wdrożeniem systemu SportRent.

## Tabela kroków i punkty bólu

| Krok | Kto | Opis czynności | Dokument / narzędzie | Problem (Punkt bólu) |
|---|---|---|---|---|
| 1 | Klient | Dzwoni lub przychodzi do punktu z pytaniem o dostępność odzieży/sprzętu w danym rozmiarze | Telefon / wizyta | Brak podglądu oferty i dostępności online |
| 2 | Pracownik | Sprawdza dostępność w zeszycie lub arkuszu kalkulacyjnym | Arkusz Excel / zeszyt | Częste błędy w stanach magazynowych, brak aktualizacji w czasie rzeczywistym |
| 3 | Pracownik | Idzie na zaplecze fizycznie sprawdzić, czy dany rozmiar jest czysty i sprawny | Magazyn | Strata czasu klienta i pracownika (10–15 min) |
| 4 | Pracownik | Jeśli brak rozmiaru — proponuje inny termin lub model | Rozmowa / telefon | Ryzyko utraty klienta |
| 5 | Pracownik | Ręcznie wypisuje umowę wypożyczenia i pobiera kaucję/opłatę | Papierowy formularz, kasa | Brak historii wypożyczeń klienta, trudne rozliczenia |
| 6 | Pracownik | Wpisuje rezerwację do arkusza i wydaje sprzęt | Arkusz Excel | Możliwość podwójnej rezerwacji (kolizje terminów) |

## Diagram (podgląd Mermaid)

```mermaid
flowchart TB
    subgraph KL["Klient"]
        S0(("Start: potrzeba wypożyczenia"))
        K1["1. Zapytaj o sprzęt i rozmiar"]
        G2{"Akceptuje zamiennik?"}
        E1((("Koniec: rezygnacja")))
        E2((("Koniec: sprzęt wypożyczony")))
    end
    subgraph PR["Pracownik wypożyczalni"]
        P2["2. Sprawdź arkusz / zeszyt"]
        P3["3. Sprawdź fizycznie na magazynie"]
        G1{"Sprzęt dostępny?"}
        P4["4. Zaproponuj inny termin/model"]
        P5["5. Wypisz umowę i pobierz opłatę"]
        P6["6. Zapisz w arkuszu i wydaj sprzęt"]
    end
    S0 --> K1 --> P2 --> P3 --> G1
    G1 -->|"nie"| P4 --> G2
    G2 -->|"tak"| P2
    G2 -->|"nie"| E1
    G1 -->|"tak"| P5 --> P6 --> E2
    classDef bol fill:#fde2e2,stroke:#c0392b
    class P2,P3,P5,P6 bol
