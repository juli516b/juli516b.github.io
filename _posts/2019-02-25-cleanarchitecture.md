---
layout: post
title: What is Clean Architecture?
subtitle: My understanding of Clean Architecture after the two first weeks.
image: /img/cleanarchitecture.jpg
comments: true
published: true
---

**What is Clean Architecture?**

Eric Evans wrote on August the 30rd 2003 the book [Domain-Driven Design: Tackling Complexity in the Heart of Software]( https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215). Eric Evans turned Software Development upside down and took a step back to look at how we design systems. Before Eric Evans book, data-centric design has been the go-to design, when designing big systems. On our education we have been introduced to Model - View model - View (MVVM) and Model - View- Controller (MVC) which puts the model in the center, which often consist of a tightly coupled database to the model. In this case, these architectures are database-centric or data-centric. 

Eric Evans turned the way of designing thinking to another level with his book. As the name implies it now was about designing with the domain in the center, instead of the data. But, what is the domain?

Imagine you are getting a new job. The hardest part of the new job is to adapt to the common rules, words used and how the routines are. This is in a sense adapting to the work’s domain. So, a domain is a field of study, where you identify and define common cohesions which in total gives a set of descriptive requirements, terminologies and functionalities that is specific for one domain or one or more subdomains. This set is not static and can be dynamically changed if changes to the domain happen. 

So, in Eric Evan's book he put this domain in the center and therefore all design thoughts should be focused around it. Therefore, as a software architect you design with the domain’s inhabitants in mind, rather than for yourself. The domain’s inhabitants are fx. The developers, the users or the buyers of the program. In a SCRUM working flow it could also be the Product owners and stakeholders. To achieve this many different approaches has been made, but the one I’m using as point of reference is **Clean Architecture**.

![alt text](https://cdn-images-1.medium.com/max/1200/0*GtcSDT7dNFshDM7c "Clean Architecture visually")

Clean Architecture is all about the SOLID principles and especially S – separation of concern. The dependency rule, as the arrows show, tells, that dependencies can only go inwards thus making the entities/use cases the center. Therefore, your abstractions, your most volatile components, are placed in the center (The business logic) and the more concrete implementations such as UI and database are placed at the outer layer making it easy for developers to switch out the database or user interface. This make the architecture independent – it does not depend on UI, Database or any other external factors because your business logic is ‘protected’ within the architecture itself. Finally, it also makes the architecture testable – since it does not depend on UI, Database etc. the business logic can be tested without these. The only thing is, that if you use a modern object relational mapper (ORM) like Entity Framework there is a need for either an abstraction layer for the ORM, or a direct dependency to the entities. 

The question to choose either a database-centric or domain-centric way of design, it all bowls down to the context and the amount of resources a company is willing to offer and the projects lifecycle. The data-centric approach might seem simple, but as complexity grows and the project comes bigger, the more data, making it more complex in the long run. Therefore, the domain-centric approach is longer termed. However, more expensive to start with. The domain way of thinking is also a lot harder to learn, since you need to learn new techniques, different approaches to different domains etc. 

In my project I will focus on a Microservice Architecture in the bigger picture. Each service will be designed domain driven with Clean Architecture. I look forward to learn more about this great stuff, and I sure hope the experiences I make on this semester is going to be invaluable to my career. 

Resources:

[Martin Fowlers website](https://martinfowler.com/)

[Enterprise Practices](https://enterprisecraftsmanship.com/2015/11/19/domain-centric-vs-data-centric-approaches-to-software-development/)

[Clean Architecture: A Craftsman's Guide to Software Structure and Design]( https://www.amazon.com/Clean-Architecture-Craftsmans-Software-Structure/dp/0134494164)


