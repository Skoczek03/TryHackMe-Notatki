# 🌐 Podstawy Web Hackingu

Moje notatki z modułu "Introduction to Web Hacking" na platformie TryHackMe.

## 1. Ręczny Przegląd Aplikacji (Walking An Application)
Zanim użyjesz automatycznych skanerów, ręcznie przejrzyj strukturę aplikacji, aby zrozumieć jej działanie.

* **Pokaż źródło strony (`Ctrl+U`):** Szukaj ukrytych komentarzy (``), notatek zostawionych przez deweloperów lub fragmentów starego kodu.
* **Narzędzia Deweloperskie (`F12`):**
    * **Inspector:** Pozwala podglądać i modyfikować kod HTML po stronie klienta (np. aby odblokować wyszarzone przyciski lub ominąć limity znaków w formularzach).
    * **Network Tab:** Służy do monitorowania wszystkich zapytań wysyłanych do serwera. Pozwala wykryć wywołania API, nagłówki i ukryte parametry przesyłane w tle.

## 2. Odkrywanie Treści (Content Discovery)
Techniki pozwalające znaleźć pliki i katalogi na serwerze, do których nie prowadzą żadne linki na stronie głównej.

### Sprawdzanie Ręczne (Manual Checks)
* `/robots.txt`: Plik z instrukcjami dla robotów Google. Często deweloperzy wpisują tam ścieżki, których *nie chcą* indeksować (np. `/admin`, `/backup`), co jest dla nas wskazówką.
* `/sitemap.xml`: Mapa witryny, która wymienia listę poprawnych, publicznych podstron.
* **Nagłówki HTTP:** W odpowiedziach serwera (np. `Server: Apache/2.4`) można znaleźć informacje o wersji oprogramowania.
* **Favicon Database:** Obliczenie hasha ikony `favicon.ico` i sprawdzenie go w bazie OWASP pozwala zidentyfikować framework używany przez stronę (np. inna ikona dla Django, inna dla Spring).

### Narzędzia Automatyczne (Automated Tools)
Służą do metody brute-force – sprawdzają tysiące nazw katalogów ze słownika (wordlisty), aby zobaczyć, które z nich istnieją (zwracają kod 200 lub 403, a nie 404).

#### Gobuster (Tryb Dir)
Bardzo szybkie narzędzie napisane w języku Go.
* `-u`: Adres URL celu.
* `-w`: Ścieżka do listy słów (np. popularna lista `common.txt`).

```bash
gobuster dir -u http://ADRES_IP_MASZYNY -w /usr/share/wordlists/dirb/common.txt
