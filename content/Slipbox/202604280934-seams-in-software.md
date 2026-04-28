---
title: Seams in software
tags:
  - slipbox
publish: true
---

> [!NOTE] Definition
>  “A seam is a place where you can alter behavior in your program without editing in that place”.



## [Legacy Seam (Martin Fowler)](https://martinfowler.com/bliki/LegacySeam.html)

- When working with a legacy system it is valuable to identify and create seams: places where we can alter the behavior of the system without editing source code.
- Each seam comes with an enabling point: “a place where you can make the decision to use one behavior or another”
- As the final example suggests, the best mechanism to use for a seam depends very much on the language, available frameworks, and indeed the style of the legacy system. Getting a legacy system under control means learning how to introduce various seams into the code to provide the right kind of enabling points while minimizing the disturbance to the legacy software.
- The best mechanism for adding seams to a legacy system may be different to what we'd do for similar flexibility in a green field.
- Feathers's book focuses primarily on getting a legacy system under test, as that is often the key to being able to work with it in a sane way.
- Once we have a seam, we are in the position to place probes into the legacy system, allowing us to increase the observability of the system.
- Effective legacy displacement is founded on introducing seams into the legacy system, and using them to gradually move behavior into a more modern environment.
- Much of my design advice is about building software with appropriately placed seams, so we can easily test, observe, and enhance it. If we write our software with testing in mind, we tend to get a good set of seams, which is a reason why Test Driven Development is such a useful technique.