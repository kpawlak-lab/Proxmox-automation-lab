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
