# morpheus

[![Build Status](https://travis-ci.org/emanuele-falzone/morpheus.svg?branch=master)](https://travis-ci.org/emanuele-falzone/morpheus)

The aim of this repository is to containerize [morpheus](https://github.com/opencypher/morpheus), the project from [opencypher](https://www.opencypher.org/) previously known as [Cypher](https://neo4j.com/developer/cypher-query-language/) for [Apache Spark](https://spark.apache.org).

#### Usage

```docker run -d -p 8888:8888 -p 4040:4040 emanuelefalzone/morpheus```

The morpheus image opens SparkUI (Spark Monitoring and Instrumentation UI) at default port `4040`, this option map `4040` port inside docker container to `4040` port on host machine . Note every new spark context that is created is put onto an incrementing port (ie. `4040`, `4041`, `4042`, etc.), and it might be necessary to open multiple ports. For example: ```docker run -d -p 8888:8888 -p 4040:4040 -p 4041:4041 emanuelefalzone/morpheus```
