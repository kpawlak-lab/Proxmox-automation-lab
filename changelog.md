Dzień 1: 23.03.2026

    Pobranie obrazu OPNsense i ręczne wyciągnięcie pliku ISO z archiwum bz2 przy użyciu 7-Zip.

    Dodanie mostka sieciowego vmbr1 w Proxmox do stworzenia odizolowanej sieci SOC LAN.

    Instalacja OPNsense na systemie plików ZFS.

    Przypisanie interfejsów: WAN pod vtnet0 i LAN pod vtnet1.

    Konfiguracja adresu IP LAN na 192.168.1.1 i uruchomienie serwera DHCP.

    Postawienie maszyny wirtualnej z Kubuntu i wpięcie jej do vmbr1.

    Zalogowanie się do panelu OPNsense przez przeglądarkę pod adresem https://192.168.1.1.

    Przejście przez Wizard, ustawienie DNS na 8.8.8.8 i 1.1.1.1.

Problemy i rozwiązania:

    Problem: Błąd w Wizardzie przy DNS (nieprawidłowy segment sieci). Rozwiązanie: Usunięcie pustych pól pod wpisanymi adresami IP.

    Problem: Brak wyjścia na świat z wnętrza laboratorium. Rozwiązanie: Wyłączenie blokowania sieci prywatnych (RFC1918) na WAN, aby OPNsense mógł komunikować się z domowym routerem i przekazywać internet.

Status: Sieć działa, Kubuntu ma internet, laboratorium jest odizolowane.
Dzień 2: 24.03.2026

    Zabezpieczenie środowiska: Wykonano snapshoty (migawki) maszyn OPNsense i Kubuntu w Proxmoxie po weryfikacji poprawnego działania sieci SOC LAN.

    Instalacja Targetu: Wdrożenie maszyny wirtualnej z Windows Server 2022 Standard (Desktop Experience).

    Konfiguracja sieci (Windows): Przypisanie statycznego adresu IP 192.168.1.10 w sieci vmbr1. Ustawienie OPNsense (192.168.1.1) jako bramy oraz serwera jako własnego DNS (127.0.0.1).

    Wdrożenie Active Directory: Zmiana nazwy hosta na DC01. Instalacja roli AD DS i promowanie serwera na Kontroler Domeny w nowym lesie soc.local.

Status: Sieć posiada aktywny Kontroler Domeny gotowy do generowania logów (Event ID) i przyjmowania ataków.
