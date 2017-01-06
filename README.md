# ApacheFlink

Apache Flink is a new trend in the stream processing industry, its the next generation engine that provides real time streaming as well as batch processing. Unlike Spark, Flink's core engine is based on distributed streaming dataflows (Streaming Engine) where as spark's core engine is a batch engine which is not stream based and hence is not naturally ideal for stream processing. Spark let you do streaming at micro batch level (let you process data every few seconds as batch - not event based) which many consider major reason behind many companies reinvesting in Flink. 

Flink also has less configuration options and handles memory management natively and completely elimintates OOM errors. This will be my quick start to try it and provide differences.

[lets get started](http://www.slideshare.net/sbaltagi/stepbystep-introduction-to-apache-flink)   
[Free training by Data Artisans](http://dataartisans.github.io/flink-training)



Also like read info on Apache Flink from data-artisan by Jamie Grier.

## Apache Flink vs Apache Spark vs Apache Storm
You can use exising Spark and Storm applications on top of Flink - but you may not achieve streaming benefits with spark.   

Two compatibility options:   
* With little modifications to the existing code you can redeploy and run the existing code on top of Flink
* Embed the existing nuts and bolts of your core code and embed it into Flink program

Spark core is developed in Scala, where as Flink is developed in Java but its other components like Gelly is built in scala. Both support Java and Scala.

## Apache Beam and Apache Flink
This is a great combination as Apache Beam provides a unified API for handling batch and streaming which can be run on Flink, Spark and Google DataFlow Service. (Google dataflow is a commercial service for batch and streaming), while Spark has some limitations for time based windowing in case of stream processing. Apache Flink, as it provides both batch and streaming Engine, is an ideal combination to provide a a complete solution.

Apache Beam provides a unified API for both batch and streaming.   
Apache Flink has a processing engine and also provides two separate API   
* DataSet API - for batch processing
* DataStream API - for stream processing 

Apache Beam --> Apache Flink 

