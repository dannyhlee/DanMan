#### IEEE Definition of Software Engineering

(1) The application of a systematic,disciplined,quantifiable approach to the development,operation and maintenance of software; that is, the application of engineering to software.

(2) The study of approaches as in the above statement.

- Systematic - a process is involved
- Disciplined - a predictable output
- Quantifiable - there are metrics and measurements

#### Lifecycle Phases

- Requirements - stakeholders discuss and capture requirements from stakeholders, through interviews, discussions, workshops, etc.
- Design - high level design of software and system to be able to be able to deliver each requirement, risk's are discussed, team capabilities, constraints thought of
- Coding/Build - Bringing reality by coding, unit testing according to design
- Testing - Testing if software functions as desired, defects are fixed and tested again
- Deployment/Implementation - Software is fully tested and high priority issues are removed and deployed to customers
- Maintenance - Once a version is released to production, the support team does maintenance

#### Software Development Lifecycle Model

- Waterfall (systematic)
  - Deliverables at each stage
  - Requirements are clear 
  - System is prepared before hand and is a reference
  - Requirements gathering, Analysis & Design, Construction, Testing, Deployment phases
- Prototyping (building archetypes)
  - building a model of system
  - could be used as-is or with refinements
  - built in increments which are working and demonstrable
  - may take time and budget
- Spiral (focuses on risks)
  - Plan - determine objectives and identify constraints
  - Risk Analysis - identify alternatives and resolve risks
  - Evaluate - review and release
  - Develop - code and test next version
  - A meta-model creating iterive stages
- Rapid Application Development (focuses on fast development)
  - Good for small projects and small teams, with tight deadlines
  - Based on prototyping and iterative development. 
  - Rapid cycles of development and release
  - focus on gather requirements, and gathering feedback
  - Continuous integration and rapid delivery
  
  #### Project Roles
  - Sponsor: Provides budget and makes high level decisions
  - Business: Provides functional requirements and if the deliverables meet requirements
  - Project manager: Brings required ppl together and manages budget and communication b/w stakeholders
  - Architect: Plans structure and interactions at high level
  - Designer: Build models and etailed design of user experience
  - Software devs: Translate design to working solutiopn
  - Software tester: Tests ssoftware meets expected requirements
  - Operations or support: 
    - L1 support- interacts directly with clients and customers
    - L2 support - solves more technical problems
    - L3 support - more complex issues and infrastructure

---

## Gathering requirements

- Gather the requirements from stakeholders through interviews, workshops, questionnaires, task analysis, observation, brainstorming, prototyping, scenario identification
- Classify and analyse the gathered requirements.
- Create requirement specification document to solidify understanding of requirements (Software Requirements Specification - SRS)
- Verify that the gathered, analysed and documented requirements match the stakeholders requirements fully.

Requirements should be: necessary, concise, unambiguous, consisten, complete, implementable, testable, traceable, identifiable.

## Design

When designing a set of guidelines to engineer quality software some ways to ensure maintainability and reliability are:
- Abstraction (reducing details, ignoring irrelevant, focusing on important aspects)
- Encapsulation (hiding complexity and internals, separating implementation from interface and hiding details unnecessary for the end user)
- Modularization (Breaking the problem into smaller component pieces)

## Testing

- Unit testing: Tests a particular mdodule to see if it meets its design spec (done by dev)
- Integration testing: Tests whether integrated module(s) meet the high level design spec (done by dev team/test team)
- System testing: Tests the system for functional and non-functional requirements (done by test team)
- Acceptance testing: Tests whether software meets end-user requirements (customer)

Bottoms up testing: Unit B calls sub units D and E.
Top-down testing: Unit F (Stub) responds to unit C.

Non-functional testing breaks down into:
- Performance testing
  - Load testing (identify max operating capacity)
  - Endurance testing (determine if system can sustain continous expected load and detect mem leaks)
  - Stress testing (determine system stability, breaking point and safe usage limits)
  - Spike testing (determine system ability to endure dramatic surges in load)
- Security testing
- Reliability testing
- Usability testing
---

### Agile 

1. Priority one, delight the customer through early and continuous delivery of valuable software
2. Welcome change, even at late stages, using Agile processes to provide to the customer's competitive advantage.
3. Continously deliver working software, every few weeks to few months, with preference to the former timeline.
4. Developers and Business must work together daily, throughout the project, to improve success.
5. The most efficient and effective method of conveyuing information to and within a development team is a face-to-face conversation.
6. Build projects around motivated individuals.  Give them the environment and support they need and trust them to get the job done.
7. Working software is the primary measure of progress.
8. Agile processes promote sustainable development.  The sponsors, developers and users should be able to maintain a constant pace indefinitely.
9. Continuous attention to technical excellence and good design enchances agility.
10. The best architectures, requirements and designs emerge from self-organizing teams.
11. At regular intervals, the teams reflects on how to become more effective, then tunes and adjusts its behavior accordingly



