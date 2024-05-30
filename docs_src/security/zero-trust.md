# Zero Trust

## Introduction

Zero Trust is a set of security strategies centered around the fundamental principle that no network is safe. There are
numerous vendors, all using the "zero trust" adjective to describe their security solutions. At the core of zero trust
are a few fundamental principles:

* Explicit Authorization: connections should be authenticated before traffic can be sent
* Cryptographically Verifiable Identities: connections should be authenticated using strong identities
* Least Privilege Access: identities should have access only the minimum set of services they require
* Continual Authentication: authorized connections should be able to be revoked immediately and monitored continuously

With version 3.2+, EdgeX Foundry can now secure its core services with a zero trust configuration. EdgeX Foundry has
integrated with [OpenZiti](https://openziti.io) to provide secure, zero trust connectivity among the EdgeX provided
services based on go. This includes the core services, support services, application services and numerous device
services.

## About OpenZiti

OpenZiti is an open source project focused on bringing zero trust networking principles directly into any application.
It accomplishes this by providing [numerous SDKs](https://openziti.io/docs/reference/developer/sdk/) that can be
integrated into any application. EdgeX Foundry has integrated the [golang sdk](https://github.com/openziti/sdk-golang/)
from the OpenZiti project, enabling secure connectivity through an OpenZiti overlay mesh network. OpenZiti also provides
clients for all major desktop and mobile operating systems that allow applications which are not OpenZiti-enabled to
access the overlay network called tunnelers. If an OpenZiti SDK cannot be integrated into an application that needs to 
connect to services secured via OpenZiti, such as the core EdgeX Foundry services, these clients can be used to provide
access. These applications are known as tunnelers.

An OpenZiti overlay network consists of a controller and edge routers. The controller, as it sounds, is responsible for
decisions surrounding the overlay network such as authentication, authorization, management of the overlay, etc. Edge
Routers are responsible for creating the overlay mesh network. One or more can link together to form a fully redundant
mesh and routers may be assigned specific roles as needed. The full scope of what OpenZiti is and how to use it is
impossible to document succinctly here. Please visit the official docs site at https://openziti.io/docs and for help,
ask in the official support forum: https://openziti.discourse.group/

## Integrating EdgeX With OpenZiti

EdgeX has adopted and integrated OpenZiti into it's microservice architecture and can now be enabled through the
standard EdgeX configuration.


zero trust overlay network


be configured for has chosen to use OpenZiti as the 

There are
a considerable number of zero-trust-praciti and no
network traffic should be considered. Zero trust
identifies 

traffic should be
permitted without first identifying 
principles that 




Zero Trust is a security framework that operates on the principle that no entity, whether inside or outside the network perimeter, should be automatically trusted. Instead, every access request must be verified and authenticated. The core principles of Zero Trust include:

Verify Explicitly: Always authenticate and authorize based on all available data points, including user identity, location, device health, service or workload, data classification, and anomalies.

Least Privilege Access: Limit user access with just-in-time and just-enough-access (JIT/JEA), risk-based adaptive policies, and data protection to help secure data and productivity.

Assume Breach: Minimize the blast radius and segment access. Verify end-to-end encryption and use analytics to gain visibility, drive threat detection, and improve defenses.

In a Zero Trust model, security is maintained by continually verifying the trustworthiness of every request as though it originates from an open network. This approach reduces the risk of internal and external threats by implementing strict access controls and continuously monitoring and validating access.

