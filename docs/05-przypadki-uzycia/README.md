# Przypadki użycia (PU) — System SportRent

## 1. Diagram przypadków użycia (UML)

```mermaid
flowchart LR
    subgraph Aktorzy
        K([Klient])
        P([Pracownik wypożyczalni])
        A([Administrator])
        S([System płatności online])
    end

    subgraph System_SportRent [System wypożyczalni sprzętu sportowego SportRent]
        PU01((PU-01: Przeglądanie katalogu i dostępności))
        PU02((PU-02: Rezerwacja sprzętu online))
        PU03((PU-03: Płatność i kaucja))
        PU04((PU-04: Wydanie sprzętu klientowi))
        PU05((PU-05: Zwrot sprzętu i rozliczenie kaucji))
        PU06((PU-06: Zarządzanie bazą sprzętu i cennikiem))
        PU07((PU-07: Przedłużenie rezerwacji))
    end

    K --> PU01
    K --> PU02
    K --> PU03
    K --> PU07

    P --> PU04
    P --> PU05
    P --> PU01

    A --> PU06
    A --> PU01

    PU02 -.->|«include»| PU01
    PU02 -.->|«include»| PU03
    PU03 --- S
    PU07 -.->|«extend»| PU02
