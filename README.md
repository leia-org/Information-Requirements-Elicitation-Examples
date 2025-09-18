# Information Requirements Elicitation Examples
This repository indexes and describes the example exercises availables for the information requiremente elicitation with LEIAs (Learning Enabling Intelligent Assitants).


## Exercise 1: Ticketing & Theathres management application

In this exercise, the user must identify the information requirements of a ticketing and teathres management application.
The expected output is a conceptual model expressed as a UML class diagram in mermaid syntax as shown below:


* **<a href="https://workbench.leia.ovh?email=_test_b25&code=RMEWO1XRAK73U2YC4" target="_blank">Demo Link</a>** to the interview exercise on the ticketing ant theatres management platform.

* **Exercise code:** RMEWO1XRAK73U2YC4

* **Context:** Tickets should be a simple platform where customers buy tickets to attend shows in theaters. You have been hired to gather the requirements for an online ticket platform.  You need to obtain these requirements by conversing with Sara Aran, the theater owner of a company that owns many theaters. The ultimate goal is to create the conceptual model of this platform using mermaid diagram syntax.

* **Solution:**
 ```mermaid
classDiagram
    class Customer {
        name
    }

    class Purchase {
        date
    }

    class Item {
        price
    }

    class Ticket {
        code
    }

    class Service {

    }

    class ServiceType {
        name
        price
    }

    class ShowDate {
        date
        time
    }

    class Show {
        name
    }

    class Theater {
        name
        location
    }

    class SeatingZone {
        name
    }

    class SeatingZonePrice {
        price
    }

    class Seat {
        row
        number
    }

    Customer "1" --> "*" Purchase
    Purchase *--> "1..*" Item
    Item <|-- Ticket
    Item <|-- Service
    Service "*" --> "1" ServiceType
    Show "1" --> "1..*" ShowDate
    Theater "1" --> "*" ShowDate
    Theater *--> "*" SeatingZone
    SeatingZone *--> "1..*" Seat
    Ticket "*" --> "1" Seat
    Ticket "*" --> "1" ShowDate
    ShowDate "1" --> "*" SeatingZonePrice
    SeatingZone "1" --> "*" SeatingZonePrice
```
