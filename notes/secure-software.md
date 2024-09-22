# Creating Secure Software

- Security is enforcing a policy that describes rules for accessing resources
  - resource is data, devices, the system itself
- Security is a system property, not a feature
- Safety (protecting against accidental risks)
- Security (protect against intentional malicious actions)

- Security objectives (**CIA**)
  - **confidentiality** (risk of disclosure)
  - **integrity** (data altered -> data worthless)
  - **availability** (service is available as desired and designed)

- Total security is unachievable
- A trade-off: more security often means higher cost / less convenience
- Security measures should be as invisible as possible

- Is a particular security measure good?
  - What problem does it solve?
  - How well does it solve the problem?
  - What new problems does it add?
  - What are the economic and social costs?
  - Given the above, is it worth the costs?

- HEP:
  - known organizations = a tempting target
  - large clusters with high bandwidth – a good place to launch further attacks
  - the potential damage could cost a lot

- **Threat Modeling and Risk Assessment**
  - Threat modeling: what threats will the system face?
  - Risk assessment: how much to worry about them?
  - risk = probability * impact

- **Protection, detection, reaction**
  - Better to protect that to recover
  - Detection is necessary because total prevention is impossible to achieve
  - Without some kind of reaction, detection is useless

- Security through obscurity ?
  - Hiding design or implementation details to gain security
  - Systems should be secure by design, not by obfuscation

- Social engineering threats
  - Exploiting human nature - weakest element
  - Understandable security policies and procedures
  - Education
  - Software shouldn’t let people do stupid things
  - Think as user

- Security is a process, not a product
  - Security should be foreseen as part of the system from the very beginning, not added as a layer at the end
- Threats (and solutions) are not only technical

- Architecture:
  - Modularity
  - Isolation
  - Defense in depth
  - Simplicity

- Golden rules
  - Make security-sensitive parts of your code small
  - Least privilege principle
  - Choose safe defaults
  - Deny by default
  - Limit resource consumption
  - Fail gracefully and securely

- Input data
  - **Don’t trust input data**
  - "Nearly every active attack out there is the result of some kind of input from an attacker. Secure programming is about making sure that inputs from bad people do not do bad things."
  - SQL injection
    - parametrized SQL queries
  - Validation:
    - dangerous until validated
    - default deny (regular expressions)
    - bounds / length checking
    - validate at entry point and before security decisions
  - Buffer overflow
    - input > memory

- Coding advice
  - Separate data from code
  - Deal with errors / exceptions
  - Protect passwords
  - Temporary files
    - symbolic link attack
    - race condition / hostile env
    - use unique name
    - use directories not writable to everyone
  - Tools: pychecker

## Summary

- Security in each phase of software dev
- Build defense in depth
- Least privilege rule
- Malicious input = worst enemy