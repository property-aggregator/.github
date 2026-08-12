# Agregator Ofert Nieruchomości

## Opis projektu
Aplikacja jest agregatorem ofert nieruchomości z różnych portali. Użytkownik otrzymuje powiadomienia o ofertach spełniających wybrane przez niego kryteria wyszukiwania.

Aplikacja przechowuje podstawowe informacje o nieruchomościach (link, pierwsze zdjęcie, cena, lokalizacja, metraż, liczba pokoi, typ nieruchomości), natomiast do pełnych szczegółów oferty użytkownik jest przekierowywany na oryginalny portal źródłowy.

### Przepływ danych
`Scraper (Python)` ➔ `Kolejka (RabbitMQ)` ➔ `API (.NET)` ➔ `PostgreSQL (PostGIS)` ➔ `Frontend (Next.js)`

---

## Use Cases

### MVP
* Rejestracja i logowanie użytkowników
* Przeglądanie i filtrowanie ogłoszeń (lokalizacja, cena, metraż, typ nieruchomości itp.)
* Archiwum ofert
* Historia zmian ceny
* Lista ulubionych nieruchomości
* Powiadomienia o ofertach (definiowanie kryteriów, powiadomienia e-mail / SMS w wersji premium)

### Planowane
* Wyszukiwanie po mapie (promień X km / zaznaczenie obszaru na mapie)
* Zakup wersji premium (dostęp do powiadomień SMS)
* Porównanie ceny z transakcjami RCN
* Analiza średnich cen i wykrywanie okazji cenowych

---

## Technologie
* **Scraping:** Python (BeautifulSoup)
* **Kolejka komunikatów:** RabbitMQ
* **Backend API:** ASP.NET Core (C#)
* **Baza danych** PostgreSQL z rozszerzeniem PostGIS
* **Frontend:** Next.js (React) - SSR / SSG

---

## Kwestie Prawne
Podczas projektowania i scrapingu uwzględniane są:
* Prawa autorskie
* Ochrona bazy danych (UE – prawo *sui generis*)
* RODO (ochrona danych osobowych)
* Przepisy o nieuczciwej konkurencji
