# Analiza Make or Buy — SportRent

**Projekt:** System wypożyczalni sprzętu sportowego  
**Wersja dokumentu:** 1.0  
**Status:** Wstępna analiza

## 1. Cel dokumentu

Celem dokumentu jest przeprowadzenie analizy Make or Buy dla wybranych elementów systemu SportRent.

Analiza pozwala określić, które funkcjonalności powinny zostać zaprojektowane i wykonane samodzielnie przez zespół projektowy (Make), a które mogą zostać oparte na istniejących rozwiązaniach, bibliotekach lub narzędziach zewnętrznych (Buy).

## 2. Kryteria wyboru

Podczas podejmowania decyzji uwzględniono następujące kryteria:

- Koszt wdrożenia i utrzymania.
- Czas potrzebny na implementację.
- Możliwość dostosowania rozwiązania do wymagań projektu.
- Bezpieczeństwo i niezawodność.
- Łatwość integracji z pozostałymi komponentami systemu.
- Możliwość dalszego rozwoju.

## 3. Analiza Make or Buy

| Element systemu | Możliwe rozwiązanie | Decyzja | Uzasadnienie |
|---|---|---|---|
| Zarządzanie sprzętem | Własny moduł aplikacji | Make | Funkcjonalność stanowi podstawową część systemu i musi być dostosowana do wymagań SportRent. |
| Rejestracja wypożyczeń | Własny moduł aplikacji | Make | Proces wypożyczania jest główną funkcjonalnością systemu. |
| Rejestracja zwrotów | Własny moduł aplikacji | Make | Obsługa zwrotów wymaga uwzględnienia reguł biznesowych projektu. |
| Zarządzanie klientami | Własny moduł aplikacji | Make | Dane klientów muszą być powiązane z wypożyczeniami. |
| Baza danych | PostgreSQL | Buy | Wykorzystanie istniejącego systemu zarządzania relacyjnymi bazami danych ogranicza konieczność tworzenia własnego rozwiązania. |
| Backend | Java Spring Boot | Buy | Wykorzystanie istniejącego frameworka przyspiesza tworzenie aplikacji i zapewnia gotowe mechanizmy. |
| Interfejs użytkownika | HTML, CSS, JavaScript | Make | Interfejs zostanie zaprojektowany i wykonany zgodnie z potrzebami użytkowników SportRent. |
| Kontrola wersji | Git i GitHub | Buy | Gotowe narzędzia umożliwiają współpracę zespołową, kontrolę zmian i przegląd kodu. |
| Testowanie | JUnit | Buy | Gotowy framework umożliwia przygotowanie i automatyzację testów jednostkowych. |

## 4. Uzasadnienie głównych decyzji

### Make — rozwiązania tworzone samodzielnie

Zespół zdecydował się samodzielnie zaimplementować najważniejsze funkcjonalności biznesowe systemu, takie jak:

- Zarządzanie sprzętem sportowym.
- Rejestrowanie wypożyczeń.
- Rejestrowanie zwrotów.
- Zarządzanie danymi klientów.

Są to kluczowe elementy projektu, dlatego ich samodzielna implementacja pozwoli dostosować działanie systemu do określonych wymagań funkcjonalnych i reguł biznesowych.

### Buy — wykorzystanie gotowych rozwiązań

W przypadku infrastruktury i narzędzi programistycznych zespół planuje wykorzystać istniejące rozwiązania:

- PostgreSQL jako system zarządzania bazą danych.
- Java Spring Boot jako framework backendowy.
- GitHub jako platformę do przechowywania kodu i współpracy.
- JUnit jako narzędzie do testowania.

Wykorzystanie gotowych technologii pozwoli ograniczyć czas implementacji i skupić się na najważniejszych funkcjonalnościach systemu.

## 5. Wstępne podsumowanie

Na podstawie przeprowadzonej analizy zdecydowano, że podstawowa logika biznesowa systemu SportRent zostanie wykonana samodzielnie przez zespół projektowy.

Do realizacji projektu zostaną wykorzystane istniejące technologie i narzędzia, które ułatwią tworzenie, testowanie i rozwijanie aplikacji.

Przedstawione decyzje mają charakter wstępny i mogą zostać zmienione w kolejnych etapach projektu.

## 6. Otwarte kwestie

- Czy system będzie wymagał zewnętrznego dostawcy usług hostingowych?
- Czy w przyszłości planowana jest integracja z zewnętrznym systemem płatności?
- Czy system będzie wymagał dodatkowych usług do wysyłania powiadomień e-mail?
