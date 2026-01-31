# 🌐 DNS & Enumeracja subdomen

Moje notatki z pokoju "Subdomain Enumeration" (ścieżka Junior Penetration Tester).

## 1. Dlaczego szukamy subdomen?
Enumeracja subdomen to proces znajdowania poprawnych adresów (np. `dev.strona.com`, `admin.strona.com`) dla danej domeny głównej.
* **Cel:** Zwiększenie powierzchni ataku. Często subdomeny deweloperskie są słabiej zabezpieczone niż strona główna.
* **Metody:** Pasywne (OSINT - bez kontaktu z celem) oraz Aktywne (Brute-force - odpytywanie serwera).

---

## 2. OSINT (Metody Pasywne)
Szukanie informacji publicznie dostępnych, bez wysyłania pakietów bezpośrednio do celu.

### Certyfikaty SSL/TLS (crt.sh)
Każdy certyfikat SSL jest rejestrowany w publicznych logach (Certificate Transparency). Możemy tam znaleźć subdomeny, dla których wygenerowano certyfikat.
* **Strona:** [crt.sh](https://crt.sh)
* **Metoda:** Wpisz nazwę domeny (np. `tryhackme.com`) i szukaj w wynikach.

### Google Dorking
Zaawansowane użycie wyszukiwarki Google do filtrowania wyników.
* `site:*.tryhackme.com` - pokaże wszystkie zaindeksowane subdomeny.
* `-site:www.tryhackme.com` - wyklucza główną domenę z wyników, pokazując tylko te mniej oczywiste.

---

## 3. Metody Automatyczne & Brute-Force
Użycie narzędzi do automatycznego odpytywania DNS lub zgadywania nazw subdomen przy użyciu słowników.

### Sublist3r
Szybkie narzędzie napisane w Pythonie, które agreguje wyniki z wielu źródeł (Google, Yahoo, Virustotal itp.).
```bash
# Podstawowe użycie
python3 sublist3r.py -d przyklad.com

# Użycie z konkretnymi portami i wątkami
python3 sublist3r.py -d przyklad.com -p 80,443 -t 50
