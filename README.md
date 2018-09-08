# deps: Maven Dependency Jars Collector

*deps* is a small shell script for collecting dependency jars for several maven artifacts. It downloads all jars depended by projects to a directory.

Useful for when you need to manually copy dependencies of some library say to an application server. Or you just want to check how many JARs or how much MBs of jars will a single library bring to your project. 

Under cover It uses Maven's dependency plugin. But you don't need to write a pom.xml 

## Usage 

$ deps `<groupId> <artifactId> <version>` 

or for multiple libraries:

$ deps `<groupId1> <artifactId1> <version1>...<groupIdN> <artifactIdN> <versionN>  ` 
 
## Example

`$./deps org.apache.zookeeper zookeeper 3.4.8 org.apache.kafka kafka-clients 0.10.1.1`

`Gathering dependencies. This may take a while...`

`SUCCESS: Dependency jars ready under deps_zookeeper-3.4.8_kafka-clients-0.10.1.1`


`deps_zookeeper-3.4.8_kafka-clients-0.10.1.1` folder contains: 
_jline-0.9.94.jar, kafka-clients-0.10.1.1.jar, log4j-1.2.16.jar, lz4-1.3.0.jar, netty-3.7.0.Final.jar, slf4j-api-1.6.1.jar, slf4j-log4j12-1.6.1.jar, snappy-java-1.1.2.6.jar, zookeeper-3.4.8.jar_

## Dependencies

Bash, Maven

## Installation

`curl -O https://raw.githubusercontent.com/rouleur/deps/master/deps`

`chmod +x deps`


