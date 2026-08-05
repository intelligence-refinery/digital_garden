---
title: Event interception
tags:
  - workbench
  - architectural-pattern
---
## In a Nutshell
When building a [[transitional-architecture|transitional architecture]], incoming events/messages/events are copied to the new system, so existing functionalities can be maintained in the legacy system while the new system is tested. 

Instead of using CDC to replicate events post-processing to the new system, this pattern can be used to accurately capture state changes from the source.

Examples
- Forking events from point-of-sale systems before they're written to a mainframe
- Forking payment transactions before they're written to a core banking system
- Publish an `OrderPlaced` event from the monolithic order processing system and have outside-in microservices subscribe to it

**Resources**
https://www.thoughtworks.com/de-de/radar/techniques/event-interception




## Diving Deeper


## 


https://martinfowler.com/articles/patterns-legacy-displacement/event-interception.html