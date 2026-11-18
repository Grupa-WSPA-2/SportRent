# Procesy biznesowe — SportRent

Katalog zawiera modele procesów biznesowych przed wdrożeniem systemu (**AS-IS**) oraz po jego wdrożeniu (**TO-BE**).

## Lista procesów

| ID | Nazwa procesu | Typ | Plik opisu | Diagram źródłowy | Eksport |
|---|---|---|---|---|---|
| P-00 | Wypożyczenie sprzętu i odzieży (obecny proces) | AS-IS | [P-00-wypozyczenie-as-is](P-00-wypozyczenie-as-is) | `P-00-wypozyczenie-as-is.bpmn` | `P-00-wypozyczenie-as-is.svg` |
| P-01 | Wypożyczenie sprzętu sportowego online | TO-BE | [P-01-wypozyczenie-sprzetu.md](P-01-wypozyczenie-sprzetu.md) | `P-01-wypozyczenie-sprzetu.bpmn` | `P-01-wypozyczenie-sprzetu.svg` |
| P-02 | Zwrot sprzętu i weryfikacja stanu | TO-BE | [P-02-zwrot-sprzetu.md](P-02-zwrot-sprzetu.md) | `P-02-zwrot-sprzetu.bpmn` | `P-02-zwrot-sprzetu.svg` |

## Konwencje modelowania
- Główny proces TO-BE (`P-01`) zamodelowano w notacji **BPMN 2.0** (narzędzie: bpmn.io / draw.io).
- Tory w ramach puli reprezentują role z naszego słownika (Klient, Pracownik wypożyczalni, System SportRent).
- Systemy zewnętrzne (Bramka płatności, Serwer poczty e-mail) przedstawiono jako osobne pule zwinięte połączone przepływem wiadomości.
