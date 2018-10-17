# Introduction

JMS was developed by Sun Microsystems to provide a way for Java programs to access an enterprise messaging system, 
also known as message oriented middleware (MOM). 
MOM provides a mechanism for integrating applications in a loosely coupled,
flexible manner by providing asynchronous delivery of data between applications in an indirect way through an intermediary.

# Pre-Requisites 
To execute and test the programs, you need access to a vendor implementation of JMS. Most Java 2 Enterprise Edition (J2EE) vendors provide an implementation of JMS. 
See your vendor documentation for setting up the JMS runtime and executing programs.
`Some of your programming decisions will depend on the JMS version in use`


#How it works
Enterprise messaging systems, often known as message oriented middleware (MOM), provide a mechanism for integrating applications in a loosely coupled, flexible manner.
They provide asynchronous delivery of data between applications on a store and forward basis; 
that is, the applications do not communicate directly with each other, but instead communicate with the MOM, which acts as an intermediary.

#Message Flexibillity 
The MOM routes the message to Application B, which can exist on a completely different computer; 
the MOM handles the network communications. If the network connection is not available, 
the MOM will store the message until the connection becomes available, and then forward it to Application B.
Another aspect of flexibility is that Application B might not even be executing when Application A sends its message. 
The MOM will hold the message until Application B begins execution and attempts to retrieve its messages. 
This also prevents Application A from blocking while it waits for Application B to receive the message.

#Publish and subscribe
Originally, enterprise messaging systems were developed to implement a point-to-point model (PTP) in which each message produced by an application is received by one other application.
In recent years, a new model has emerged, called publish and subscribe (or pub/sub).

Pub/sub replaces the single destination in the PTP model with a content hierarchy, known as topics. 
Sending applications publish their messages, indicating that the message represents information about a topic in the hierarchy.
Applications wishing to receive those messages subscribe to that topic. 
Subscribing to a topic in the hierarchy that contains subtopics allows the subscriber to receive all messages published to the topic and its subtopics.

#JMS overview and architecture
JMS clients. Java programs that send and receive messages using the JMS API.
Non-JMS clients. It is important to realize that legacy programs will often be part of an overall JMS application, and their inclusion must be anticipated in planning.
Messages. The format and content of messages to be exchanged by JMS and non-JMS clients is integral to the design of a JMS application.
JMS provider. As was stated previously, JMS defines a set of interfaces for which a provider must supply concrete implementations specific to its MOM product.
Administered objects. An administrator of a messaging-system provider creates objects that are isolated from the proprietary technologies of the provider.

