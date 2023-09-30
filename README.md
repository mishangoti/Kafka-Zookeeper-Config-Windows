# Steps to Install and Configure Apache Kafka on Windows

## Steps 1 : Download Kafka from official website an Unzip it.
[Kafka Download Link](https://kafka.apache.org/downloads).
![This is an alt text.](/images/pic_1.PNG "This is a sample image.")

## Step 2 : Change the fonfiguration in Zookeeper and Server property file.
Open file 1 
  * C:\kafka\config\server.properties
  * Edit line number 63 -> add custom path to save logs
  * C:/kafka/tmp/kafka-logs
            
Open file 2 
  * C:\kafka\config\zookeerer.properties
  * Edit line number 16 -> add custom path to save logs
  * C:/kafka/tmp/kafka-logs

## Step 3 : Start the Zookeeper
Open new terminal
  * C:\kafka on CMD/teminal
  * Run command
  * .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

## Step 4 : Start the kafka server.
Open new terminal 
  * C:\kafka on CMD/teminal
  * run command
  * .\bin\windows\kafka-server-start.bat .\config\server.properties

## Step 5 : Create a topic.
Open new terminal 
  * C:\kafka on CMD/terminal
  * Run commad
  * .\bin\windows\kafka-topics.bat --create --topic myFirstTopic --bootstrap-server localhost:9092
    * Output: Created topic myFirstTopic

## Step 6 : Start Kafka Producer.
Open new terminal
  * C:\kafka on CMD/terrminal
  * Run command
  * .\bin\windows\kafka-console-producer.bat --topic myFirstTopic --bootstrap-server localhost:9092
  * > From here you can write any message to in that perticuler TOPIC

## Step 7 : Start Kafka Consumer.
Open new terminal
  * C:\kafka on CMD/terminal
  * Run command
  * .\bin\windows\kafka-console-consumer.bat --topic myFirstTopic --from-beginning --bootstrap-server localhost:9092
  * > here you will recieved message what ever is Produced from Producer.
