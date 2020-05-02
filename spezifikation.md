TODO 
 - Workflow mit developer branch besprechen
 - Authentication in gRPC
 - Authentication zwischen MS
 - Serverside discovery(?) Namensauflösung
 - Adressen einzelner Services(?)

Wir haben uns die folgende Spezifikation überlegt:
 - Identifikatoren verwenden UUIDs(String) anstelle Serieller-Typen(long/Bigint).
 - Die Synchrone-Kommunikation zwischen den MS im Backend findet in gRPC statt.
 - Die Asynchrone-Kommunikation zwischen den MS im Backend findet als Messaging mit Kafka in JSON statt.
 - Alle MS besitzen eine eigene UUID und Erkennungsobjekt, damit Services eindeutig identifiziert werden können.
 - Alle MS arbeiten mit UUIDs als Referenz auf Daten anderer MS (z. B. UserUUID als Referenz für Userdaten).
 - Userdaten werden ausschließlich von dem Bürgerbüro verwaltet und können mittels userUUID abgefragt werden.
 - MS speichern in ihren Datenmodellen ausschließlich die userUUID anstelle spezifischer Daten.
 - API-Modelle(DTOs) und Schnittstellen sind im Pflichtenheft einheitlich als JSON zu spezifizieren.

Die Schnittstellen müssen im Pflichtenheft vollständig definiert werden, sodass ersichtlich wird wie andere Teilnehmer 
mit diesen kommunizieren können.

Datenobjekte sollten als JSON wie im folgenden Beispiel definiert werden:
```json
   "sgse.models.einwohnermeldeamt.user": {
      "description": "Represents a user for the einwohnermeldeamt",
      "fields": [
        { "name": "userId", "type": "string", "required": true },
        { "name": "firstName", "type": "string", "required": true },
        { "name": "lastName", "type": "string", "required": true }
      ]
    }
```
