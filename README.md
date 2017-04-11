# EclipsePahoMavenExample
An example Maven Project that uses Eclipe Paho to publish a message to an MQTT broker over websockets.

## Build and Run

 * To build: ```mvn package```
 * Then to run it: ```java -cp target/my-app-1.0-SNAPSHOT-jar-with-dependencies.jar org.eclipse.paho.App```

## Change Dependency Version
The ```pom.xml``` file currently references the Paho release repository.
To use the SNAPSHOT release, change the repository url to: ```https://repo.eclipse.org/content/repositories/paho-snapshots/``` and change the dependency version to: ```1.1.2-SNAPSHOT```.


## Change the Protocol
This example publishes a message over websockets by default. To change the protocol, change the server URI in [this](src/main/java/org/eclipse/paho/App.java) source file.

 * tcp - Normal TCP Connection
 * ssl - SSL / TLS Connection
 * ws - WebSockets
 * wss - WebSockets over SSL/TLS
