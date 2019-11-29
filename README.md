Avro Schemas
============

Denne modulen inneholder Avro-filer som beskriver hvordan meldingene serialiseres og 
deserialiseres på kafka topic mellom soknadsmottaker.

- Topic mellom soknadsmottaker og soknadsarkiverer benytter `src/main/avro/JournalpostArkiv.avsc`

Java-koden blir generert i `generate-sources`-fasen.

Topic config
============

`src/main/topicconfig/` inneholder konfigurasjonsfilene som ble brukt til å opprette topicene.
Dersom man har behov for å gjenopprette topics så gjør man følgende:
- Gå til swagger siden for [kafka-adminrest](https://kafka-adminrest-q4.nais.preprod.local/api/v1/apidocs/index.html?url=swagger.json#/)
- Naviger til "oneshot"
- Kopier json fra config filen til ønsket topic
- Paste json inn og trykk execute
- Sjekk responskode/output

NB! Dersom man sletter og gjenoppretter topics må man huske å legge til riktige personer i KM gruppen.
