# Restful Booker API Tests

## Opis projektu

Projekt testów API wykonany w narzędziu Postman dla aplikacji Restful Booker.

Celem projektu było praktyczne przećwiczenie testowania REST API, tworzenia automatycznych asercji, zarządzania danymi testowymi, wykorzystania zmiennych środowiskowych oraz mechanizmu Request Chaining.

Projekt obejmuje scenariusze pozytywne, negatywne, walidacyjne oraz testy Smoke.

---

## Wykorzystane technologie

* Postman
* REST API
* JavaScript
* Environment Variables
* Dynamiczne dane testowe
* Request Chaining
* Automatyczne asercje

---

## Struktura projektu

### Auth

Testy odpowiedzialne za uwierzytelnianie użytkownika oraz generowanie tokenu dostępu.

### Smoke Tests

Podstawowe testy sprawdzające dostępność oraz najważniejsze funkcjonalności API.

### Booking Positive

Scenariusze pozytywne obejmujące pełny cykl CRUD:

* Create Booking
* Get Booking
* Update Booking
* Delete Booking
* Verify Delete

### Booking Negative

Scenariusze negatywne sprawdzające zachowanie API dla niepoprawnych operacji:

* Invalid Login
* Empty Login
* Update Without Token
* Delete Without Token
* Non Existing Booking

### Booking Validation

Testy walidacyjne sprawdzające poprawność obsługi danych wejściowych:

* Missing Fields
* Empty Values
* Long Firstname
* Invalid Date Format
* Negative Price
* Special Characters

---

## Funkcjonalności

* Testowanie autoryzacji
* Testy Smoke
* Testy CRUD
* Testy negatywne
* Testy walidacyjne
* Dynamiczne dane testowe
* Zmienne środowiskowe
* Request Chaining
* Automatyczne asercje
* Czyszczenie danych testowych

---

## Request Chaining

W projekcie wykorzystano mechanizm Request Chaining polegający na przekazywaniu danych pomiędzy kolejnymi zapytaniami.

Przykłady:

* zapisanie tokenu po uwierzytelnieniu i wykorzystanie go w kolejnych operacjach wymagających autoryzacji,
* zapisanie identyfikatora bookingId po utworzeniu rezerwacji i wykorzystanie go w operacjach GET, PUT oraz DELETE.

---

## Zidentyfikowane problemy

Podczas wykonywania testów walidacyjnych zidentyfikowano następujące potencjalne problemy:

### Niepoprawny format daty

API akceptuje niepoprawny format daty i zamiast zwrócić błąd walidacji generuje nieprawidłową wartość:

0NaN-aN-aN

### Brak ograniczenia długości pola firstname

API akceptuje bardzo długie wartości w polu firstname bez zastosowania ograniczeń długości oraz bez zwrócenia błędu walidacji.

### Ujemna wartość rezerwacji

API akceptuje ujemne wartości w polu totalprice, mimo że cena rezerwacji nie powinna być mniejsza od zera.

### Ograniczona walidacja danych

Część niepoprawnych danych wejściowych jest akceptowana i zapisywana w systemie zamiast zostać odrzucona odpowiednim kodem błędu HTTP.

---

## Statystyki projektu

* Liczba requestów: 20+
* Liczba automatycznych testów: 70+
* Testy Smoke
* Testy pozytywne
* Testy negatywne
* Testy walidacyjne

---

## Uruchomienie projektu

1. Zaimportuj kolekcję Postman.
2. Zaimportuj środowisko (Environment).
3. Wybierz środowisko testowe.
4. Uruchom kolekcję za pomocą Collection Runner.
5. Przeanalizuj wyniki wykonanych testów.

---

## Autor

Aleksandra Janas

Projekt portfolio Junior QA Engineer.

