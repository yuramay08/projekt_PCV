# Dokumentácia k projektu

## Popis projektu
V tomto projekte som navrhol a implementoval základnú sieť so serverom poskytujúcim služby HTTP a FTP. Topológia siete je hviezdicovitá so switchom, ku ktorému sú pripojené dva počítače a server. 

## Konfigurácia siete
- **IP adresy zariadení:**
  - Server: `192.168.1.1`
  - Počítač 1: `192.168.1.2`
  - Počítač 2: `192.168.1.3`
- **Maska siete:** `/24` (255.255.255.0)

## Konfigurácia FTP servera
- **Vytvorené používateľské kontá:**
  - `admin0` s právami RWDNL (plný prístup).
  - `user0` s právami R (iba čítanie).

Používatelia môžu pristupovať k serveru cez FTP klienta pomocou svojich poverení.

## Konfigurácia HTTP servera
HTTP server bol nakonfigurovaný na poskytovanie základnej webovej stránky. Súbor `index.html` bol upravený a obsahuje jednoduchú štruktúru s hlavičkou, navigačným menu, hlavným obsahom a pätou.

## Testovanie siete
- **Ping:** Overená dostupnosť všetkých zariadení v sieti pomocou príkazu `ping`.
- **FTP:** Pripojenie a operácie na FTP serveri boli úspešne otestované.
- **HTTP:** Webová stránka je prístupná cez prehliadač na adrese `http://192.168.1.1`.

## Bezpečnostné riziká
1. **FTP server:** Prenos údajov nie je šifrovaný, čo predstavuje riziko zachytenia poverení.
2. **HTTP server:** Dátová komunikácia cez HTTP nie je šifrovaná, čo môže viesť k odpočúvaniu.
3. **Sieťová topológia:** Absencia firewallu alebo segmentácie môže umožniť neautorizovaný prístup.

## Možné vylepšenia
- Zavedenie HTTPS na webovom serveri.
- Použitie SFTP namiesto FTP pre bezpečný prenos súborov.

---

# Project Documentation

## Project Description
This project involves designing and implementing a basic network with a server providing HTTP and FTP services. The network topology is star-shaped with a switch connected to two computers and a server.

## Network Configuration
- **Device IP Addresses:**
  - Server: `192.168.1.1`
  - PC 1: `192.168.1.2`
  - PC 2: `192.168.1.3`
- **Subnet Mask:** `/24` (255.255.255.0)

## FTP Server Configuration
- **Created User Accounts:**
  - `admin0` with RWDNL rights (full access).
  - `user0` with R rights (read-only).

Users can connect to the FTP server using their credentials via an FTP client.

## HTTP Server Configuration
The HTTP server was configured to host a basic web page. The `index.html` file was customized to include a simple structure with a header, navigation menu, main content, and footer.

## Network Testing
- **Ping:** Verified connectivity between all devices in the network using the `ping` command.
- **FTP:** Successfully tested connection and operations on the FTP server.
- **HTTP:** The web page is accessible via a browser at `http://192.168.1.1`.

## Security Risks
1. **FTP Server:** Data transfer is unencrypted, posing a risk of credential interception.
2. **HTTP Server:** Communication over HTTP is unencrypted, making it susceptible to eavesdropping.
3. **Network Topology:** Lack of a firewall or segmentation may allow unauthorized access.

## Potential Improvements
- Enable HTTPS on the web server.
- Use SFTP instead of FTP for secure file transfer.
