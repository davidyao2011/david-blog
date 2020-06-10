---
title: Web Service
date: "2019-09-20T21:12:03.284Z"
description: "In the beginnings of computing, software systems were isolated systems which were totally self-sufficient, monolithic programs running on a mainframe system that included a database."
---

## Service-Oriented Architecture

![webservice](./web-service.jpg)

As you have read earlier, as computing evolved, organisations moved to smaller applications on a variety of systems, and developed various mechanisms for those applications to share information  and to communicate with each other. This "distributed architecture" was mostly within the same organisation, and sometimes with other partner organisations, and was often custom-built.

In today's world, there are myriads of software systems and applications, running on a huge range of platforms, that are wanting to interact with each other, either over an private newtork or over the internet. One way to enable this interaction is to adopt a **service-oriented architecture**.

**A Service Oriented Architecture (SOA)** is a form of distributed systems architecture which:
provides an abstract logical view of services provided by software systems (independent of the inner workings and platform of the application) uses messages to request services and provide responses
provides a machine-readable description of services offers a small number of operations per service, with large and complex messages communicates over a network is platform-neutral.
Source: W3 Consortium, 2004, 3.1 [Service-Oriented Architecture](https://www.w3.org/TR/ws-arch/#service_oriented_architecture).

Several implementations of this service-oriented architecture were developed, such as CORBA. One of them is the Web services approach which, as its name implies, operates over the Internet. According to W3C's Service-Oriented Architecture Working Group there are two classes of web services:

- **REST-compliant web services** - follow the REST architecture, which is based on HTTP and where a service. exposes a standard set of stateless operations
- **Arbitrary Web services** - where the service may expose an arbitrary set of operations.

If you are interested in the history of service-oriented architecture, watch this video:
[Exploring the history of web services](https://www.linkedin.com/learning/programming-foundations-web-services/exploring-the-history-of-web-services) (Gassner, linkedin.com, 2013).

---

## Web Services

### Types of Web Services

Two very common forms of web services are the **SOAP web services** and the **RESTful APIs**.

### What are Soap Services?

"SOAP is a standard communication protocol for exchanging structured messages between computer systems in the XML-based message format. It stands for Simple Object Access Protocol and defines a set of rules associated with messages being sent from one system to another, and a response message is received by this other system. Some key concepts are associated with SOAP services; WSDL (Web Services Description Language) is a standard way of defining a directory of SOAP-based services, message format, and other required information. "
-- Mahmoud, 2018

---

### What are RESTful Web Services?

RESTful web services are lightweight, lossly coupled web services that are well suited for creating APIs for clients spread out across the internet. Representational State Transfer is an architectural style of client-server application centered around the transfer of representations of resources through requests and responses. In the REST architectural style, data and functionality are considered resources and are accessed using Uniform Resource Identifiers, typically links on the Web. The resources are represented by documents and are acted upon by using a set of simple, well-defined operations.

---

## Webhooks

### Introducing Webhooks

Webhooks are simple callbacks that are rapidly growing in popularity with a lot of developers. Webhooks work in a very similar way to Lambda functions; they are invoked when a particular event is fired by an application on the web. This makes them highly applicable to a variety of web development use cases where, rather than having a traditional API that polls for data on a frequent basis, you use a Webhook to get data at real time.

With most APIs there's a request followed by a response, whereas in the case of Webhooks, they simply send the data whenever it's available.

The way a Webhook works is quite simple! To use a Webhook, you register a URL with the Webhook provider, for example IFTTT or Zapier. The URL is a place within your application that will accept the data and do something with it. In some cases, you can tell the provider the situations when you'd like to receive data. Whenever there's something new, the Webhook will send it to your URL.

### Example

Here's a common example of a Webhook--open up any of your GitHub pages from your browser. There, in your repository's Setting page, you will see a Webhooks section as shown in the following image.
You can always add a new Webhook to your repository by selecting the Add webhook option. There, you can provide a URL that will receive an event each time you either push or commit code into your repository and so on.

On the event getting triggered, GitHub sends a POST request to the URL with details of the subscribed events. You can also specify which data format you would like to receive the request in, for example, JSON or x-www-form-urlencoded . In this way, you can easily create open ended integrations with other arbitrary web services without having to spin up any new infrastructure or manage any complex code integrations as well.
-- Gupta & Wadia (2017)

### A webhook consists of

- A subject – the resource that generates the events. Currently, this resource is the repository where you create the webhook.
- One or more events – the default event is a repository push, but you can select multiple events that can trigger the webhook.
- A URL – the endpoint where you want Bitbucket to send the event payloads when a matching event happens.
  There are two parts to getting a webhook to work:
  1. Creating the webhook
  2. Triggering the webhook

After you create a webhook for an event, every time that event occurs, the provider sends a payload request that describes the event to the specified URL. Thus, you can think of webhooks as a kind of notification system. Source: Atlassian webhook documentation
