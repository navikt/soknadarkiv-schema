# Avro Schemas
This repo contains Avro-files that define how the messages are serialized and deserialized on the Kafka topics.

For a description of the whole archiving system, see [the documentation](https://github.com/navikt/archiving-infrastructure/wiki).

- The topic used between [Soknadsmottaker](https://github.com/navikt/soknadsmottaker) and [Soknadsarkiverer](https://github.com/navikt/soknadsarkiverer) is using the schema definition in `src/main/avro/Soknadarkivschema.avsc`

The Java code is being generated in the `generate-sources` phase of the Maven execution.

## Usage
[![](https://jitpack.io/v/navikt/soknadarkiv-schema.svg)](https://jitpack.io/#navikt/soknadarkiv-schema)

To use the generated Java classes, include the repo as a dependency using [JitPack](https://jitpack.io/#navikt/soknadarkiv-schema/89a9c7a). To use the latest schema definitions, use the sha of the latest commit as the dependency version.

## Topic config
The directory `topicconfig/` contains the configuration files that were used to create the topics in [kafka-adminrest](https://kafka-adminrest.nais.preprod.local/api/v1/).


## Inquiries
Questions regarding the code or the project can be asked to [team-soknad@nav.no](mailto:team-soknad@nav.no)

### For NAV employees
NAV employees can reach the team by Slack in the channel #team-fyllut-sendinn
