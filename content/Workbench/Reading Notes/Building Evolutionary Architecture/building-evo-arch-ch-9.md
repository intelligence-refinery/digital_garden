---
title: 9 – Putting Evolutionary Architecture into Practice
tags:
  - reading-notes
  - book
  - architecture-design
  - workbench
publish: true
---
# Premise
- The steps required to implement the ideas around evolutionary architecture

# Interesting asides
- Platform teams are meant to provide a “compelling internal product” to accelerate delivery by stream-aligned teams
- Book recommendation: *Project to Product* (Kersten) #book-recommendation
- [[strangler-fig|Strangler Fig Pattern]]
- "Demonstration defeats discussion"


# 9.1 - Organizational factors
## 9.1.1 – Don’t fight Conway’s Law
- Careful of too many coupling/integration points between teams  
	- So each team can function independently, just like services
- How a group breaks down a problem affects the choices that can be made later  
- System design tends to be copies of communication structures in an org  
- Functional silos lead to optimization of immediate tasks within each silo, resulting in components may not work well together  
- Recommend structuring teams around service boundaries to ↓ operational friction, as has all the roles needed to own all needed changes 
- Cross-functional teams ↓ coordination friction & engenders ownership  
- Need to account for cognitive load on a single team  
- [[202604260742-think-products-not-projects|Think in terms of products, not projects]] → long-term ownership of quality  
- Create small (“2 pizza”) teams to limit communication overhead  


## 9.1.2 – Culture
- Architects should be aware of:
	- What behavior the org rewards  
	- Design approaches for how devs build systems  
	- Teach & encourage devs to build evolutionary architecture skills  
- Adjusting team behavior often requires adjusting team processes  
	- “Tell me how you measure me, and I will tell you how I will behave.”  
- If a team is unaccustomed to change, introduce practices that normalize it  
	- When adopting a new library/framework:
	  - Run small experiments to explicitly evaluate coupling impact  
	  - Ex: Can devs write/test code outside the framework?



## 9.1.3 – Culture of experimentation
- Successful experimentation = regularly running small activities to try new ideas & integrating successful ones  
- Ways to encourage experiments:
	- Get ideas from external sources  
	- Encourage explicit improvement  
	- Generate [[202604260751-spike-solutions|spike solutions]]
	- Increase confidence in estimates  
	- Create innovation time  
	- Set-based development:
	- Explore multiple options simultaneously via quick prototypes  
	- Connect devs with end users  



## 9.1.4 – CFO & Budgeting
- With ↑ number of quanta, ↓ marginal cost (to a point)  
- Architects must understand trade-offs between evolvability & inherent uncertainty  



# 9.2 – The business case

## 9.2.1 – Hypothesis & data-driven development
- Use FFs to test hypotheses  
- End users are part of the feedback cycle  
- Example:
  - Make an icon 5% larger → measure impact via A/B testing  
- Requires ability to run multiple versions simultaneously  
- Prefer measurement over surveys  



## 9.2.2 – FFs as experimental media
- Use FFs to test hypotheses  
- See case studies  



# 9.3 – Building enterprise FFs
- Role of enterprise architect:
  - Guide purposeful coupling points  
  - Guide platform choices  
  - Enable enterprise-wide FFs  



## 9.3.1 – Case study: 0-day security vulnerability
- Deployment pipelines include a “slot” for security team FFs  
- Enables standardized testing when vulnerabilities appear  

**Key:**
- Pipelines should alert teams to ecosystem changes:
  - Code  
  - DB schema  
  - Deployment config  
  - FFs  

- Enables automated governance of cross-cutting concerns:
  - Security  
  - Scalability  
  - etc.  



## 9.3.2 – Carving out BCs in existing architecture
- Identify domain-specific regions  
- Use FFs to prevent unwanted coupling  



# 9.4 – Where do you start?
- Low-hanging fruit  
- Areas already loosely coupled  
- Demonstrate value quickly with concrete data  
- Prioritize highest value first  
- Show long-term value of evolutionary architecture  



# 9.5 – Future state
- Generative testing  
- Common in functional programming  



# 9.6 – Why (or why not?)

### Why
- Scalability ≈ evolvability  
- Advances business capabilities via testing  
- ↓ cycle time  
- Flexibility to choose best architecture per context  
- Avoid tech debt from adaptation  

### Why not
- Other concerns dominate  
- Sacrificial architecture  



## Testing
- Add coarse-grained functional tests  
- Catch regressions during restructuring  



## Infrastructure
- Enable fast, incremental changes  



## Notable quote
> “Controlling coupling & automating verification is the key to building well-governed architectures that can evolve via domain, technical change, or both.”