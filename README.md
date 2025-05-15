# Distribution-Center-Logistics-System

## Overview

This project models and implements a business process integration scenario for a large consumer goods company, **Uniprocterlevergamble**, focusing on the **Distribution Center**'s role in managing truck logistics, staging, and delivery coordination. The system was developed using **Mendix** and integrates various stakeholders including **Transport Companies**, a **Control Tower**, and external APIs.

## Business Case

The process starts when an order is received by Uniprocterlevergamble, triggering a chain of activities:
- Request and evaluation of transport quotes
- Transportation order issuance
- Load sharing if necessary
- Coordination of truck arrival, staging, loading, and departure
- Real-time truck location tracking
- Delivery confirmation

The BPMN model included reflects this full end-to-end workflow.

## Objectives

- Build a working Mendix application modeling the distribution center's process.
- Support full order lifecycle management and truck logistics.
- Integrate external systems using **REST**, **SOAP**, and **OData**.
- Enable real-time tracking via APIs and simulate integration readiness using dummy apps.

## Architecture and Technologies

- **Mendix** low-code platform (core development)
- **REST / OData APIs** for external integration
- **Draw.io** for BPMN modeling
- **Postman** for API testing
- **World Time API** for real-time scheduling data

## Key Components

### Internal Logic
- Truck staging, queuing, and capacity management
- Order assignment and loading processes
- Real-time status updates and error handling

### External Integration
- **Data Retrieval** from Control Tower via REST
- **Truck Ready Notifications** via REST POST request
- **Truck ETA Notifications** via OData (simulated with dummy app)
- **Time API Integration** for ETA scheduling

## BPMN Models

- Full end-to-end process model of Uniprocterlevergamble's logistics flow
- Detailed BPMN of the Distribution Center’s primary processes

> BPMN files available in the repository:  
> - `BPMN of the whole business process.png`  
> - Referenced in project documentation PDF

## Testing Instructions

- Use Postman to POST truck and order data to `/rest/share-eta`
- Use Postman to test `truck-ready` notifications via `/rest/notify-truck-ready`
- Trigger truck ETA updates from dummy Mendix project (CT_dummy_App)
- Use city input to retrieve current time using the Time API

## Project Contributors

- Miglena Pavlova
- Gabriela Todorova  
- Dani Mahaini  
- Alan Nessipbayev  
