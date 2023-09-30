# Steps to Install and Configure Apache Kafka on Windows

## Steps 1 : Download Kafka from official website an Unzip it.
[Kafka Download Link](https://kafka.apache.org/downloads).
![This is an alt text.](/images/pic_1.PNG "This is a sample image.")

## Step 2 : Change the fonfiguration in Zookeeper and Server property file.
Open file 1 : C:\kafka\config\server.properties
            : edit line number 63 -> add custom path to save logs
            : D:/kafka/tmp/kafka-logs
Open file 2 : c:\kafka\config\zookeerer.properties
            : edit line number 16 -> add custom path to save logs
            : D:/kafka/tmp/kafka-logs

## Step 3 : Start the Zookeeper
Open new teminal  : C:\kafka on CMD/teminal
                  : run command
                  : .\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties

## Step 4 : Start the kafka server.
Open new teminal  : C:\kafka on CMD/teminal
                  : run command
                  : .\bin\windows\kafka-server-start.bat .\config\server.properties

## Step 5 : Create a topic.


## Step 6 : Start Kafka Producer.


## Step 7 : Start Kafka Consumer.

*This text will be italic*  
_This will also be italic_

**This text will be bold**  
__This will also be bold__

_You **can** combine them_







# Markdown syntax guide

## Headers

# This is a Heading h1
## This is a Heading h2 
###### This is a Heading h6

## Emphasis

*This text will be italic*  
_This will also be italic_

**This text will be bold**  
__This will also be bold__

_You **can** combine them_

## Lists

### Unordered

* Item 1
* Item 2
* Item 2a
* Item 2b

### Ordered

1. Item 1
1. Item 2
1. Item 3
  1. Item 3a
  1. Item 3b

## Images

![This is an alt text.](/image/sample.png "This is a sample image.")

## Links

You may be using [Markdown Live Preview](https://markdownlivepreview.com/).

## Blockquotes

> Markdown is a lightweight markup language with plain-text-formatting syntax, created in 2004 by John Gruber with Aaron Swartz.
>
>> Markdown is often used to format readme files, for writing messages in online discussion forums, and to create rich text using a plain text editor.

## Tables

| Left columns  | Right columns |
| ------------- |:-------------:|
| left foo      | right foo     |
| left bar      | right bar     |
| left baz      | right baz     |

## Blocks of code

```
let message = 'Hello world';
alert(message);
```

## Inline code

This web site is using `markedjs/marked`.
