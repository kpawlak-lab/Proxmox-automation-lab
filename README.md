Automated SOC & Incident Response Lab
Cel projektu

Budowa pełnowymiarowego, symulowanego środowiska korporacyjnego do nauki Threat Huntingu i automatyzacji Incident Response. Projekt obejmuje pełną ścieżkę: od ataku, przez detekcję w SIEM, po automatyczny triage w SOAR.
Architektura i Technologie

    Hypervisor: Proxmox VE – zarządzanie infrastrukturą wirtualną.

    Network & Firewall: OPNsense – izolacja segmentu SOC LAN (192.168.1.0/24) od sieci domowej.

    Infrastruktura: Windows Server 2022 (Active Directory), Windows 11, Kubuntu (Management & Attack Node).

    Telemetria & EDR: Microsoft Sysmon – głębokie logowanie zdarzeń systemowych.

    SIEM: Splunk Enterprise – centralizacja, analiza i korelacja logów.

    SOAR: n8n – automatyzacja procesów bezpieczeństwa i komunikacja z API.

    Threat Intelligence: VirusTotal API – wzbogacanie alertów o reputację plików.

Scenariusze (Use Cases)

    Active Directory Brute-Force:

        Atakujący: Kubuntu (Hydra).

        Cel: Windows Server 2022.

        Detekcja: Monitorowanie Windows Security Event ID 4625 w Splunku.

    Automatyczny Triage (SOAR):

        Wyzwalacz: Wykrycie złośliwego skryptu PowerShell.

        Akcja: Automatyczna weryfikacja hasha w VirusTotal i raport na kanał Slack.
