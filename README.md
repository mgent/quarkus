[![Gitpod ready-to-code](https://img.shields.io/badge/Gitpod-ready--to--code-blue?logo=gitpod)](https://gitpod.io/#https://github.com/mgent/quarkus)

# quarkus project

This project uses Quarkus, the Supersonic Subatomic Java Framework.

If you want to learn more about Quarkus, please visit its website: https://quarkus.io/ .

## Running the application in dev mode

You can run your application in dev mode that enables live coding using:
```shell script
./mvnw compile quarkus:dev
```

> **_NOTE:_**  Quarkus now ships with a Dev UI, which is available in dev mode only at http://localhost:8080/q/dev/.

## Packaging and running the application

The application can be packaged using:
```shell script
./mvnw package
```
It produces the `quarkus-run.jar` file in the `target/quarkus-app/` directory.
Be aware that it’s not an _über-jar_ as the dependencies are copied into the `target/quarkus-app/lib/` directory.

If you want to build an _über-jar_, execute the following command:
```shell script
./mvnw package -Dquarkus.package.type=uber-jar
```

The application is now runnable using `java -jar target/quarkus-app/quarkus-run.jar`.

## Creating a native executable

You can create a native executable using: 
```shell script
./mvnw package -Pnative
```

Or, if you don't have GraalVM installed, you can run the native executable build in a container using: 
```shell script
./mvnw package -Pnative -Dquarkus.native.container-build=true
```

You can then execute your native executable with: `./target/quarkus-1.0.0-SNAPSHOT-runner`

If you want to learn more about building native executables, please consult https://quarkus.io/guides/maven-tooling.html.

## Related guides

- Minikube ([guide](https://quarkus.io/guides/kubernetes)): Generate Minikube resources from annotations
- Apache Kafka Client ([guide](https://quarkus.io/guides/kafka)): Connect to Apache Kafka with its native API
- YAML Configuration ([guide](https://quarkus.io/guides/config#yaml)): Use YAML to configure your Quarkus application
- Apache Avro ([guide](https://quarkus.io/guides/kafka)): Provide support for the Avro data serialization system
- Logging JSON ([guide](https://quarkus.io/guides/logging#json-logging)): Add JSON formatter for console logging
- Kubernetes ([guide](https://quarkus.io/guides/kubernetes)): Generate Kubernetes resources from annotations
- Micrometer metrics ([guide](https://quarkus.io/guides/micrometer-metrics)): Instrument the runtime and your application with dimensional metrics using Micrometer.
- Picocli ([guide](https://quarkus.io/guides/picocli)): Develop command line applications with Picocli
- DataStax Apache Cassandra client ([guide](https://quarkus.io/guides/cassandra)): Connect to Apache Cassandra databases
- Kubernetes Client ([guide](https://quarkus.io/guides/kubernetes-client)): Interact with Kubernetes and develop Kubernetes Operators
- Kubernetes Config ([guide](https://quarkus.io/guides/kubernetes-config)): Read runtime configuration from Kubernetes ConfigMaps and Secrets

## Provided examples

### YAML Config example

This Supersonic example displays mach speed in your favourite unit, depending on the specified Quarkus configuration.

[Related guide section...](https://quarkus.io/guides/config-reference#configuration-examples)

The Quarkus configuration location is `src/main/resources/application.yml`.

### Logging JSON example

This example let you go faster with your jet aircraft, your speed is logged when you send a new request.<br/> When you reach the speed of sound, a "Sonic Boom" error is going to be thrown and logged. Boom!

[Related guide section...](https://quarkus.io/guides/logging#configuration)

### Picocli Example

Hello and goodbye are civilization fundamentals. Let's not forget it with this example picocli application by changing the <code>command</code> and <code>parameters</code>.

[Related guide section...](https://quarkus.io/guides/picocli#command-line-application-with-multiple-commands)

Also for picocli applications the dev mode is supported. When running dev mode, the picocli application is executed and on press of the Enter key, is restarted.

As picocli applications will often require arguments to be passed on the commandline, this is also possible in dev mode via:
```shell script
./mvnw compile quarkus:dev -Dquarkus.args=='help'
```
