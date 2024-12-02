# Avro Schemas
This repo contains Avro-files that define how the messages are serialized and deserialized on the Kafka topics.

For a description of the whole archiving system, see [the documentation](https://github.com/navikt/archiving-infrastructure/wiki).

- The topic used between [Soknadsmottaker](https://github.com/navikt/soknadsmottaker) and [Soknadsarkiverer](https://github.com/navikt/soknadsarkiverer) is using the schema definition in `src/main/avro/Soknadarkivschema.avsc`

The Java code is being generated in the `generate-sources` phase of the Maven execution.

New version is published when changes are pushed to the main branch.

## Usage
To use the generated Java classes, include the repo as a dependency using.
```
<dependency>
	<groupId>no.nav.soknad.arkivering</groupId>
	<artifactId>avro-schemas</artifactId>
	<version>${arkivering-schemas.version}</version>
</dependency>
```
e.g. arkivering-schemas.version = 1.4.4-48e96305a5d2

In addition, include repository:
```
<repository>
	<id>github</id>
	<url>https://github-package-registry-mirror.gc.nav.no/cached/maven-release</url>
</repository>
```

## Topic config
The directory `topicconfig/` contains the configuration files that were used to create the topics in [kafka-adminrest](https://kafka-adminrest.nais.preprod.local/api/v1/).


## Inquiries
Questions regarding the code or the project can be asked to [team-soknad@nav.no](mailto:team-soknad@nav.no)

### For NAV employees
NAV employees can reach the team by Slack in the channel #team-fyllut-sendinn
