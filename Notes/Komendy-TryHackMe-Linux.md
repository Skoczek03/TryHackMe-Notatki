#  <img src="https://upload.wikimedia.org/wikipedia/commons/3/35/Tux.svg" alt="Linux Penguin" width="40"/> Lista użytecznych komend i linków 

## Linux komendy 🐧
Wszystkie komendy do Linuxa 
Link: https://www.mediacollege.com/linux/command/linux-command.html

Tłumaczenie komend Linux 
Link: https://explainshell.com

## TryHackMe komendy

Gobuster - Narzędzie do brute-forcowania subdomen
- `gobuster dns -d przyklad.com -w /usr/share/wordlists/SecLists/Discovery/DNS/common.txt`

ffuf - Służy do szybkiego fuzzingu, czyli odkrywania ukrytych katalogów, plików oraz wirtualnych hostów 
- `ffuf -w /usr/share/wordlists/SecLists/Discovery/DNS/namelist.txt -H "Host: FUZZ.acmeitsupport.thm" -u http://MACHINE_IP`

Sublist3r - Służy do automatycznego wyszukiwania subdomen przy użyciu publicznych źródeł (OSINT) 
- `python3 sublist3r.py -d przyklad.com -p 80,443 -t 50`

## Przydatne linki
- Jak znaleść subdomeny danej strony internetowej https://crt.sh
- Identyfikacja technologi strony www https://www.wappalyzer.com/
- 







 
