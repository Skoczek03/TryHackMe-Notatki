# 🛡️ Fundamenty Bezpieczeństwa i Metodologia Pentestów

Moje notatki dotyczące kluczowych zasad bezpieczeństwa informacji oraz standardowego przepływu pracy w testach penetracyjnych, oparte na ścieżce "Introduction to Pentesting" z TryHackMe.

## 1. Triada CIA (Poufność, Integralność, Dostępność)
Podstawowy model bezpieczeństwa informacji, na którym opiera się ochrona danych.

* **Confidentiality (Poufność):** Zapewnienie, że dostęp do danych mają tylko osoby uprawnione.
    * *Przykłady:* Uwierzytelnianie dwuskładnikowe (2FA), Szyfrowanie dysków.
* **Integrity (Integralność):** Gwarancja, że dane nie zostały zmienione ani naruszone przez osoby niepowołane (lub w wyniku błędu).
    * *Przykłady:* Sumy kontrolne plików (Hashing), Podpisy cyfrowe.
* **Availability (Dostępność):** Zapewnienie, że systemy i dane są dostępne wtedy, gdy są potrzebne.
    * *Przykłady:* Zapasowe zasilanie, Redundancja serwerów, Ochrona przed atakami DDoS.

## 2. Zasady Zarządzania Uprawnieniami
* **Principle of Least Privilege (PoLP - Zasada Najmniejszych Przywilejów):** Użytkownicy i systemy powinni posiadać tylko minimalny poziom dostępu niezbędny do wykonania swojego zadania.
    * *Cel:* Ogranicza to potencjalne szkody w przypadku przejęcia konta przez atakującego.

## 3. Metodologia Pentestów (Cykl Ataku)
Standardowe etapy przeprowadzania testu penetracyjnego:

1.  **Information Gathering (Rekonesans):** Zbieranie ogólnodostępnych informacji (OSINT) o celu (domeny, pracownicy, zakresy IP) bez ingerencji w system.
2.  **Enumeration / Scanning (Skanowanie):** Aktywne użycie narzędzi (np. Nmap, Gobuster) do wykrycia otwartych portów, usług i działających aplikacji.
3.  **Exploitation (Eksploitacja):** Wykorzystanie znalezionych podatności, aby uzyskać wstępny dostęp do systemu.
4.  **Privilege Escalation (Eskalacja Uprawnień):** Próba podniesienia uprawnień ze zwykłego użytkownika na Administratora lub Roota.
5.  **Post-Exploitation:** Utrzymanie dostępu (persistence), zbieranie wrażliwych danych i przeskakiwanie na inne systemy w sieci (pivoting).
6.  **Reporting (Raportowanie):** Dokumentowanie wszystkich znalezisk, ocena ryzyka oraz zalecenia naprawcze dla klienta.

## 4. Aspekty Prawne
* **Rules of Engagement (RoE):** Formalny dokument tworzony przed rozpoczęciem testów, który definiuje zakres działań (scope), dozwolone metody i ramy czasowe.
* **Ważne:** Testowanie bezpieczeństwa bez pisemnej zgody właściciela systemu jest nielegalne. **Permission is everything.**
