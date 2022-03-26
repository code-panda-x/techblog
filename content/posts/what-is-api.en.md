---
title: "What is API"
date: 2022-03-01T18:05:22-05:00
draft: false
tags: ["Web Application","API", "HTTP", "What is"]
categories: ["General Tech"]
slug: "what-is-api"
subtitle: "Ultimate API guide"
description: "Ultimate API guide"
keywords: 
- API
- HTTP
---

### What is API
Application Programming Interface: allows two applications to talk to each other

### What is REST API
REST (Representational State Transfer): A set of **functions** for developers to perform **requests** and **receive** responses using **HTTP** protocol

### Challenges under API testing
1. API Documentation (need endpoint, parameters, resources, data)
2. Access to DB (Validate response by comparing response to DB)
3. Authorization overhead (Handle tokens)

### Core components of HTTP request 
1. HTTP request methods
2. URI
3. Resources and parameters
4. Request header (JSON, XML)
5. Request body (message content)

### What is Payload
- Payload/body is secured **input** data sent to API
- In JSON

### What is JSON
- JavaScript Object Notation
- Data format represented as String-text

### Authentication Techniques used in API's
1. Session/Cookie based Authentication
2. Basic Authentication
3. Digest Authentication
4. OAuth

### Why API testing is suitable for automation testing
API testing is:
1. Light-weight
2. More stable than UI testing

### What to verify in API testing
1. Verify the accuracy of data (if is as expected)
2. Check HTTP status code
3. Response time
4. Error codes if API return errors
5. Check Authorization 
6. Non-functional testing


### Path parameter and Query parameter
    // below is an API request URL
    http:/abcd.com/orders/11234?location=IND

    // End point: http:/abcd.com
    // Resource: orders

After / : path parameter

After ? : query parameter

### API testing vs UI testing
API: back-end

UI: front-end

### Soap WebServices
Simple Object Access Protocol: it is a **XML** based message ***protocol***

### Serialization && Deserialization
Serialization: Convert **Java obj** --> **JSON** (Request body/payload)

Deserialization: Convert **JSON** --> **Java obj**

### JSON path example
    courses[0].details.site


### API calling examples
Python:
```
import requests
r = requests.get("https://www.pythonhow.com/real-estate/rock-springs-wy/LCWYROCKSPRINGS", headers={'User-agent': 'Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:61.0) Gecko/20100101 Firefox/61.0'})
c=r.content
```

Dart:
```
final response = await http.post(url, body: json.encode(requestModel.toJson())); 
print(response.headers['set-cookie']);
print(response.statusCode);

final response = await http.post(url, headers: {'Authorization': token}, body: json.encode(requestModel.toJson())); 
```

