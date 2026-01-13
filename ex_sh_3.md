# Exercise 1
## a) What should you keep in mind when it comes to architectural risk analysis? Name at least 4 things

- What valuable assests do we have?
- What are possible attack vectors that can be used to attack those assets?
      OBS: Document what was, is and will be implemented. Design flaws can be more important than code level vulnerabilities.
- Which of these attack vectors are more probable to be used?
- How can we mitigate the most probable and most severe attack vectors?
      Mitigation is important when looking at access control and Auth

## b) Name the three sections of threat modeling

 1. Determening threats
    - Determening entry points
    - Determening trust boundaries
 2. Rating threats
    - What is more serious?
    - What is more probable?
 3. Determening countermeasures
    - What can be done

## c)Think of a place where you would set boundaries and why?

The boundaries should be set between the card reader terminal and the office pc as this is the access point most likely to have a security compromise, as it could be infected with malware or other malicious processes. The pattient card is another point that could be exploited, but for that there would need to be fisical access to it which would be hard.

Between the Data Provider and the terminal, if the terminal is breached the VPN can be used to gain access to the system.

Between the Data Service and Database, so that the service only have access to the information that it needs (Least Privilege Principle)

## d) Why are threat models and architectures different?

Threat models are a way to visualize possible attacks, and create mitigations. Visualize how the data flows between components.

Architecture is the desig of the system. With multiple components being able to be one single component in the threat model.

## e) What are the aspects of Distrustful Decomposition? Why is it important to uphold them? Explain each aspect.

You will have more complex code that needs to be sanboxed, and then you have more complexity

Decompose each system, separete them

Principle of least privilege

Use inter processe comunication

Each proccess distrusts each other

# 2 Cross Site Scripting

User inject malicious code into a user field that is run in the browser when a user access that information. 