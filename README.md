# Avro Schemas
Denne modulen inneholder Avro-filer som beskriver hvordan meldingene serialiseres og deserialiseres på kafkatopic mellom soknadsmottaker og soknadsarkiverer. Dokumentasjon av [hele arkiveringssystemet](https://github.com/navikt/archiving-infrastructure/wiki).

- Topic mellom soknadsmottaker og soknadsarkiverer benytter `src/main/avro/JournalpostArkiv.avsc`

Java-koden blir generert i `generate-sources`-fasen.

Vid hver push til main så genereres automatisk en [ny pakke her](https://github.com/navikt/soknadarkiv-schema/packages/).


## Topic config
`src/main/topicconfig/` inneholder konfigurasjonsfilene som ble brukt til å opprette topicene.
Dersom man har behov for å gjenopprette topics så gjør man følgende:
- Gå til swagger-siden for [kafka-adminrest](https://kafka-adminrest.nais.preprod.local/api/v1/)
- Naviger til "oneshot"
- Kopier json fra configfilen til ønsket topic
- Paste json inn og trykk execute
- Sjekk responskode/output

NB! Dersom man sletter og gjenoppretter topics må man huske å legge til riktige personer i KM gruppen.
