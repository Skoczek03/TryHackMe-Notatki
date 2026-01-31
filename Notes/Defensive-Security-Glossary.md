# 🏰 Słownik Bezpieczeństwa Defensywnego (Blue Team)

Kluczowe pojęcia i koncepcje związane z defensywą i pracą w zespołach Blue Team.

## Role i Zespoły (Teams)
* **Red Team (Atakujący):** Specjaliści ds. ofensywnego bezpieczeństwa, którzy symulują ataki hakerskie, aby przetestować obronę firmy.
* **Blue Team (Obrońcy):** Specjaliści ds. defensywnego bezpieczeństwa odpowiedzialni za ochronę infrastruktury organizacji i reagowanie na incydenty.
* **Purple Team (Współpraca):** Podejście polegające na współpracy zespołów Red i Blue w celu wymiany wiedzy i szybszej poprawy bezpieczeństwa.

## Kluczowe Koncepcje

### SOC (Security Operations Center)
Centrum Operacji Bezpieczeństwa. To scentralizowana jednostka lub zespół monitorujący bezpieczeństwo organizacji w trybie 24/7. Ich głównym celem jest wykrywanie, analiza i reagowanie na incydenty cyberbezpieczeństwa.

### SIEM (Security Information and Event Management)
Rozwiązanie programowe, które agreguje i analizuje logi (dzienniki zdarzeń) z różnych źródeł (zapory sieciowe, serwery, antywirusy) w czasie rzeczywistym, aby wykryć podejrzaną aktywność.
* *Przykłady:* Splunk, ELK Stack, Wazuh.

### DFIR (Digital Forensics and Incident Response)
Informatyka Śledcza i Reagowanie na Incydenty.
* **Digital Forensics (Informatyka śledcza):** Proces zbierania i analizy dowodów z urządzeń cyfrowych w celu ustalenia, co dokładnie wydarzyło się podczas ataku.
* **Incident Response (Reagowanie na incydenty):** Zorganizowane podejście do zarządzania skutkami naruszenia bezpieczeństwa lub ataku cybernetycznego (procedury działania).

### Malware Analysis (Analiza Złośliwego Oprogramowania)
Proces zrozumienia zachowania i celu podejrzanego pliku (malware).
* **Static Analysis (Analiza statyczna):** Badanie kodu pliku bez jego uruchamiania (np. sprawdzanie sum kontrolnych, ciągów znaków).
* **Dynamic Analysis (Analiza dynamiczna):** Uruchamianie wirusa w bezpiecznym, odizolowanym środowisku (tzw. sandbox), aby obserwować, co próbuje zrobić (np. z jakimi serwerami się łączy). 
