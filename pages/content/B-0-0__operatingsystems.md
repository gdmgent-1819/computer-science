---
title: Besturingssystemen
title_long: Besturingssystemen
permalink: operatingsystems/
---

# Hardware

## Computers
### Supercomputers
- Enkele processoren (’60 - ’70).
- Honderden/duizenden processoren.
- Quadriljoenen berekeningen in nanoseconden.
- Honderden vierkante meters ruimte.
- Gebouwd voor specifieke doeleinden.

Voorbeelden:
- Weather and climate operational supercomputing system (foto).
    - National Oceanic and Atmospheric Administration.
    - Weer en klimaat voorspellingen.
- IBM’s Sequoia machine
    - Beveiliging van nucleaire wapens.
    - Moleculaire dynamische berekeningen.

### Mainframe computers
- Kleinere versie van supercomputers.
- Grote organisaties en bedrijven.
- Virtuele machines.
- Marktleider IBM.
- Kostprijs: 75.000 tot 10 miljoen euro.

### Minicomputer
- Jaren ’60 & ’70.
- Kleinere mainframe.
- Ondersteund tot 200 gebruikers.
- Netwerk
- Servers en microcomputer.

### Server & datacenter
- Diensten verlenen.
- Netwerk
- Klein in omvang.
- Datacenter
    - Grote hoeveelheid servers.
    - Optimale + beveiligde omgeving.
    - Racks
- Voorbeelden:
    - Webserver
    - Fileserver
    - Gameserver
    - Cloud, [filmpje: wat is de cloud?](https://www.youtube.com/watch?v=Mzl4Wud_Bp0)

### Microcomputer
- Personal computers.
- Desktop computers, laptops, video game consoles,…
- Microprocessor

### Samenvatting
- Supercomputers
    - Specifiek doeleind.
- Mainframe computers.
    - Grote bedrijven
- Minicomputer
    - Vroeger -> kleinere bedrijven
- Server & datacenter.
    - Diensten verlenen.
- Microcomputer
    - Personal computer.

## Computeronderdelen
### Inputtoestellen
- Communiceren met de computer.
- Toetsenbord, muis, joystick, controller,…
- Keyboards
    - Elke vorm van input door toetsen.
- Aanwijzende toestellen.
    - Elke manier om een punt aan te wijzen.

### Outputtoestellen
- De computer communiceert met ons.
- Weergeven van informatie.
- Hoofdtelefoon, monitor, printers,...

### Verwerkingstoestellen
- Informatie te verwerken.
- Moederbord
    - Centraal
    - Laat componenten communiceren.
    - Chipset: onderverdeeld in 2 delen namelijk Northbridge en Southbridge.
    - Northbridge
        - Snelle componenten.
            - Processor socket.
                - CVE/CPU: Centrale verwerkingseenheid of Central Processing Unit, [informatiefilmpje Dell, Computer Processors Explained](https://www.youtube.com/watch?v=lxnlyJYZ6Vw).
                    - De CPU bestaat uit 3 componenten.
                        - Memory of storage unit.
                            - Bewaart instructies, data en resultaten.
                        - Control unit.
                            - Controleert bewerkingen van andere computeronderdelen.
                        - ALU (Arithmetic Logic Unit).
                            - Arithmetic section (rekenkundige operaties).
                            - Logic section (logische bewerkingen).
                - Hersenen
                - Ophalen, decoderen en uitvoeren van instructies.
                - Uitvoeren van mathematische en logische calculaties.
                - Input data -> output data.
                - Snelheid in Gigahertz (GHz).
                - Klok die aantal keer per seconde slaat.
                    - 3.1 GHz - 3.1 biljoen per seconde.
                - Elke slag -> berekening.
                - Beïnvloed door meerdere factoren.
                - 32-bit vs 64-bit CPU
                    - 64-bit de meest moderne.
                    - Verschil in het aantal berekeningen.
                    - Kan meer data uit het geheugen behandelen.
                    - Software programmeurs.
                    - Software in 32 of 64 bit.
                    - Mac OS X heeft geen 32 bit versie meer.
            - Aansluiting geheugenmodules.
                - RAM: random access memory
                    - Tijdelijk geheugen.
                    - Elke geheugenplaats even snel toegankelijk.
                    - Lezen en schrijven kan in willekeurige volgorde gebeuren.
                - ROM: read only memory
                    - Geheugen die men gebruikt wanneer er data moet bewaard worden als het toestel uitstaat.
            - Videokaart
                - GPU: graphics processing unit, deze neemt de videotaken over van de CPU.
                - BIOS: bewaren van de settings van de grafische kaart en voert testen uit op het geheugen van de kaart bij het opstarten.
                - RAM: wanneer de GPU afbeeldingen maakt, dient hij deze samen met andere informatie te kunnen bewaren.
                    - Informatie over pixels.
                    - Kleuren
                    - Locatie ervan op het scherm.
                - Slots:
                    - PCI: Peripheral component interconnect
                    - AGP: Advanced graphics port
                    - PCIe: PCI Express, snellere communicatie tussen grafische kaart en het moederbord. Mogelijkheid tot het aansluiten vn meerdere grafische kaarten.
            - Uitbreidingskaarten
    - Southbridge
        - Trage componenten.
        - BIOS (Basic input/output system, EFI voor Mac)
            - Is een bibliotheek met basisinstructies.
            - Is de brug tussen opstarten van hardware en het opstarten van het besturingssysteem.
            - Weet waar het besturingssysteem staat.
            - Toegankelijk via bepaalde toets of toetsencombinatie.
            - Aanpassingen maken.
            - Wijzigingen opgeslagen in CMOS (Complementary Metal-Oxide-Semiconductor), grootte 256 bytes.

        - Aansluiting opslagtoestellen.
        - Aansluitingen voor toetsenbord, muis, netwerk,…


# Data
------

Het is nuttig te weten hoe hoeveelheden data uitgedrukt worden in termen van computers, hieronder een onverzicht.

| Naam     | Symbool | Verklaring                                         |
|:------  -|:-------:|---------------------------------------------------:|
| bit      | b       | bit (samentrekking van binary en digit), 0 of 1 als waarde. |
| Byte     | B       | Byte is een binaire eenheid van data, 1 Byte = 8 bits. |
| Kilobyte | kB      | 10³ bytes (ofwel 1000 bytes)                       |
|----------|---------|----------------------------------------------------|
| Megabyte | MB      | 10^6 bytes (ofwel 1.000.000 bytes)                  |
| Gigabyte | GB      | 10^9 bytes (ofwel 1.000.000.000 bytes)              |
|----------|---------|----------------------------------------------------|
| Terabyte | TB      | 10^12 bytes (ofwel 1.000.000.000.000 bytes)         |
| Petabyte | PB      | 10^15 bytes (ofwel 1.000.000.000.000.000 bytes)     |
|----------|---------|----------------------------------------------------|
| Exabyte  | EB      | 10^18 bytes (ofwel 1.000.000.000.000.000.000 bytes) |
| =========|=========|====================================================|
| Naam     | Symbool | Verklaring                                         |
{:.table.table-hover}