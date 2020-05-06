# Schnittstellen Sammmlung 

## Bürgerbüro - Pia

### Message Queues:

-   Bürger umgezogen (Adresse hat sich geändert)
    
-   Namensänderung (Vor oder Nachname hat sich geändert)
    
-   Neuer Fundgegenstand abgegeben
    

### Bietet an:

-   Gibt Userdaten raus (Benötigt UserID)
    
-   Nimmt Anhänge fürs schwarze Brett entgegen
    
-   Verifiziert User Token und gibt userid zurück
    

### Wird angefordert:

-   Alle Services - Benutzerdaten (Name, Nachname) abfragen
    
-   Rettungsdienst: Bürger für tot erklären
    

## Öffentlicher Nahverkehr (ÖPNV) - Alexander

### Message Queues:

### Bietet an:

### Wird angefordert:

## Parkplatz - Sven

### Message Queues:

### Bietet an:

-   Parkplatz reservieren
    
-   Auslastung abfragen
    
-   Parkfläche bereitstellen
    
-   Parkfläche bearbeiten
    
-   Parkfläche löschen
    

### Wird angefordert (grün = “alles ok/wird gemacht”, rot = “nicht ok/nicht vorgesehen”):

-   Restaurants - Parkplatzauslastung abfragen
    
-   Hausarzt - Parkplatz reservieren
    
-   Krankenhaus - Parkplatz reservieren
    
-   Ordnungsamt - Falschparker/Ordnungswidrigkeiten melden
    
-   Straßenverkehrsamt - Parkplatz reservieren
    

## Straßenverkehrsamt - Benedikt

### Message Queues:

### Bietet an:

-   (ggf. hat Führerschein)
    
-   (ggf. Führerschein entziehen)
    

### Wird angefordert:

## Hausarzt - Tim

### Message Queues:

### Bietet an:

-   Überweisungen von Patienten an Krankenhaus/Fitnesscenter
    
-   Krankenakte rausschicken
    

### Wird angefordert:

-   Restaurants: Terminüberschneidung überprüfen
    
-   Krankenhaus: Überweisung entgegennehmen
    
-   Krankenhaus, Rettungsdienst: Krankenakte abrufen
    
-   Krankenhaus: Krankenakte aktualisieren
    
-   Ordnungsamt: Psychisch Kranke melden
    

## Restaurants - Andre K.

### Message Queues:

### Bietet an:

-   Terminüberschneidung von Benutzer überprüfen
    

### Wird angefordert:

## Krankenhaus - Jendrik

### Message Queues:

### Bietet an:

-   Überweisung von Patienten an den Hausarzt
    
-   Entgegennahme von Überweisungen
    
-   Vereinbaren von Terminen
    
-   Teilnahme an Veranstaltungen
    

### Wird angefordert:

-   Krankenhaus: Überweisungen entgegennehmen
    
-   Krankenhaus: Krankenakte
    
-   Rettungsdienst: Patient übergeben
    

## Supermarkt - Andre M.

### Message Queues:

-   Sonderangebote(?)
    

### Bietet an:

-   Produkte Bestellen (einmalig und “Dauerauftrag”)
    

### Wird angefordert:

-   Tierarzt: Produkte bestellen(ProduktID, UserID)
    
-   Restaurants: Produkte bestellen, Bestellkatalog abfragen
    

## Fitness Center - Malte

### Message Queues:

### Bietet an:

-   Trainingsplan beantragen
    
-   Termin beim Physiotherapeut anfragen
    

### Wird angefordert:

-   Hausarzt: Info, ob UserID den Fitness Plan gemacht hat
    

## Ordnungsamt - Philipp

### Message Queues:

### Bietet an:

-   Bestehende Genehmigungen anfragen
    
-   Bestehende Ordnungswidrigkeiten anfragen
    
-   Ordnungswidrigkeit melden
    
-   Meldung von psychisch Kranken
    

### Wird angefordert:

-   Parkplatz - Falschparker melden (Ordnungswidrigkeit)
    

## Bank - Fabian

### Message Queues:

### Bietet an:

-   Geld einzahlen/auszahlen
    
-   Geld überweisen
    
-   Geld monatlich(generell Zeitlich) überweisen
    
-   Konto anlegen
    

### Wird angefordert:

-   Hausarzt: monatliche Gehaltszahlung von Hausarzt an User ID
    
-   Hausarzt: einmalige Zahlungen von User ID an Hausarzt
    
-   Parkplatz: Message für Abbuchung (Bezahlen)
    
-   Krankenhaus: einmalige Zahlungen von User ID an das Krankenhaus
    
-   Supermarkt: abbuchen von Geld von Kundenkonto
    
-   Straßenverkehrsamt: Gebühren bezahlen
    

## Tierarzt - Mattis

### Message Queues:

### Bietet an:

-   Tierarzt Termine anzeigen
    
-   Tierarzt Termine anfordern/löschen
    
-   Tierfutter/Medizin bestellen
    
-   Tierarztkosten bezahlen
    

### Wird angefordert:

-   Restaurants: Terminüberschneidung überprüfen
    

## Rettungsdienst - Patrick

### Message Queues:

-   Person verstorben
    

### Bietet an:

-   Einsatzbericht abrufen
    
-   Transport anmelden
    

### Wird angefordert:

-   Krankenhaus: Patientendaten abrufen
    
-   Ordnungsamt: Psychisch Krankentransport
    

## ÖPNV - Alex

### Message Queues:

-   Neue Verkehrsinformationen
    
-   Fahrplan Änderungen
    

### Bietet an:

-   Ticket kosten
    
-   Verkehrsinformationen
    

### Wird angefordert:

-   Bank - Geld abbuchen / zurückbuchen
    
-   Parkplatz - Wie viele freie Parkplätze (Und wo?)
    
-   Straßenverkehrsamt - User hat Führerscheinsammlung
