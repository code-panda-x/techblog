# Web Service


# What is web service
Software system designed to support interoperable machine-to-machine interaction over a network.

Three keys:
1. machine to machine (todo service is not)
2. Interoperable (not platform dependent)
3. Over a network 

## Different kinds of web services
### SOAP
Use **XML** as exchange format 

Adhere to Structure: Envelope - Header - Body

### REST

The **format** of request/response is HTTP

#### resources
A resource has an URI, it is what you want to present in your application 

A resource can have different representations
- XML
- HTML
- JSON (most popular)

Define and perfom actions on resources using HTTP
POST/GET/PUT/DELETE

---

# How to build web service 

## How does applications communicate

Application <==request, response==> web service

How to make communication platform independent?
Use data exchange format:
1. XML
2. JSON

Transport:
1. HTTP
2. MQ

## Tools
- Browser
- Curl
- Postman

Browser makes it hard to send Post/Put/Delete command, that's why we use Postman
