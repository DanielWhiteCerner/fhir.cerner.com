---
title: CapabilityStatement | R4 API
---

# CapabilityStatement

* TOC
{:toc}

## Overview

The CapabilityStatement resource documents the functionality implemented from the HL7<sup>®</sup> FHIR<sup>®</sup> standard. Unlike most resources,
this resource is found at [`:serviceRootURL/metadata`] instead of by its resource name.

## Metadata

Get the capabilities and configurations of this implementation and deployment of the FHIR standard.

    GET /metadata?:parameters

_Implementation Notes_

* Authentication is not required to access the Conformance resource
* No parameters other than the standard `_format` parameter are supported for reading CapabilityStatement

### Authorization Types

Authorization is not required.

<%= authorization_types(provider: true, patient: true, system: true) %>

### Headers

<%= headers head: {Accept: 'application/fhir+json'} %>

### Open Endpoint Example

#### Request

    GET /metadata

#### Response

<%= headers status: 200 %>
<%= json(:r4_open_metadata) %>

### Closed Endpoint Example

#### Request

    GET /metadata?_format=json

#### Response

<%= headers status: 200 %>
<%= json(:r4_auth_metadata) %>

[`:serviceRootURL/metadata`]: ../../#service-root-url
