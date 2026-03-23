Dzień 1: Instalacja Proxmox, OPNsense i Kubuntu
Co zrobiłem:

    Walka z obrazem ISO: Pobrałem OPNsense. Musiałem ręcznie wyciągnąć plik .iso z archiwum .bz2 przez 7-Zipa, bo Windows próbował go rozpakować jako folder.

    Sieć w Proxmoxie: Dodałem drugi mostek sieciowy vmbr1 (SOC-LAN). Dzięki temu mam teraz dwie osobne sieci: jedną z internetem domowym (vmbr0) i drugą, całkowicie odizolowaną dla maszyn w labie.

    Instalacja OPNsense:

        System postawiony na ZFS.

        WAN przypisany do vtnet0 (bierze net z domu).

        LAN przypisany do vtnet1 (adres 192.168.1.1).

        Włączyłem DHCP, żeby router sam nadawał adresy maszynom w labie.

    Stacja robocza Kubuntu:

        Postawiłem VM z Kubuntu i wpiąłem ją do vmbr1.

        System automatycznie dostał IP z routera.

        Potwierdziłem, że widzę panel zarządzania OPNsense przez przeglądarkę pod adresem https://192.168.1.1.

Schemat połączeń:

Internet <-> Router domowy <-> OPNsense (WAN/LAN) <-> Kubuntu
