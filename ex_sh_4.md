# Ex. 1 - Risk Assessment

## a) How is risk calculated? What is important to be kept in mind?

Risk of a given event can be calculated with the folowing equation:

    Risk(event) = probability(event) * impact(event)
    
It is important to keep in mind that people tend to **over/underestimate risks**. There are events that are really impactfull but that don't happen often, and there are events that are recurent that can have a significant impact, but don't have a observable impact.

## b) Think of an "account" that is important to you and one that is less important. Discuss the risk assessment for both and explain it.

**Important**: Main e-mail account.
Can lead to more accounts being compromised.

**Unimportant**: Login info of a service that was used once.
If there aren't any important info then the impact is low.

## c) Explain the differences between abuse cases and risk assessment.

**Abuse case** is defined to prevent a user of a system to do something they are not suposed/authorized to do. (scenario driven)

**Risk assessment** is used to determine events that may ocurre that can have a significant negative impact on the system. And it should originate from CIA and assets.


# Ex. 2 - Protection Poker
Fibonacci Numbers up to 100:

** Try to use all the numbers**

1, 2, 3, 5, 8, 13, 21, 34, 55, and 89.

| Asset Value | Data | Used in Feature
|---|---|---|
|2   |Name of employee|1,2      |
|21   |Address of employee|2   |
|1   |Employee ID|1,2   |
|55   |Banking info of employee|2      |
|8   |Personal email of employee|2    |
|5   |Work email of employee|1    |
|34   |Social security number of employee|2    |
|5   |Insurance info of employee|2    |
|1   |User access of employee|2   |
|2   |Accommodations of Employee|2    |


|Feature # | Feature | Total Value Points | Ease Points | Security Risk |
|--|--|--|--|--|
|1| Work group|8 | 13| 21 
|2| Change of employee personal information| 129| 5| 134

## Based on your assessment: Which feature seems to have the highest risk?
The change of employee personal data, seeing that it needs a bunch of important personal information.

# Ex. 3 - Risk-Driven Test Planning (RDTP)
## a) What are the goals of RDTP?
- Mitigate negative impact
- Create mitigation strategies early
- Smoth out the usage of the product, by mitigating disruptions

## b) Explain how Top-Down Test Planning works.

1. Broad domain analysis

    - Goals
    - Assets

2. Risks

    Knowing the goals, the risks can be derived from what could stop us from achieving the goals.

3. Indicators

    Define what could show us that a high-level risk manifested
    - Is the system misbehaving?
    - Metrics are off?
    - Systems are down?

4. Tests

    Given an indicator, how do we ensure that the indicator is avoided or satisfied?

## c) Explain how Buttom-Up Security Test Planning works.

1. Write tests
    - Should be short form
    - Just ideas

2. Group them into categories
    - Assets, functionality, CIA consequences, etc.

3. Revise the categories
    - Are there groups missing?
    - Are there tests missing inside a group?

4. Add more tests

## Diferences between the two aproaches

### Top-down
- Is tied to specific goals
- Might be imcomplete or not cover some inter-goal tests.
- Might lead to less creative tests (checklist way of thinking)

### Bottom-up
- Gives more freadom to create different test
- Might miss a categorie(s)
- Requires more experience

# Ex. 4 - Vulnerability of the Day


## Log overflow 

[Incident Postmortem: Outdated NGINX Server and Log Overflow](https://medium.com/%40abel.sekibaala/incident-postmortem-outdated-nginx-server-and-log-overflow-5c9b8d98633b)

Porly configured/outdated version of NGINX was running, without log rotation.

[FortiOS and SSL Vulnerabilities](https://www.fortinet.com/blog/psirt-blogs/fortios-ssl-vulnerability)

## Path traversal

# References

## [Risk analysis in software design](https://www.blackduck.com/blog/software-risk-analysis.html)

It's important to "apply classic risk definitions to software design and then generate accurate mitigation requirements".

"Software vulnerabilities come in two basic flavors: **flaws** (design-level problems) or **bugs** (implementation-level problems). Automated scanners tend to focus on bugs, since human expertise is required for uncovering flaws."

### Flaws
    Design level problems, bad definition, bad domain level design

### Bugs
    Implementation level, bad code, bad dependencies, OS vulnerabilities.

"risk analysis is **not a science**, and broad knowledge of vulnerabilities, bugs, flaws, and threats is a critical success factor."

"white board level" design is required to have a overview of the system and find possible vulnerabilities

Divide in 3 categories: must haves, important to haves, and nice but unnecessary.

Legal requirements are always a must have.

### Mitigations
Some risks can be controled through some mitigations. Others can only dampen the risk impact.

### Limitations
Will probably not provide a exaustive list of all the risks. 

Might need to analyse on a component-by-component, tier-by-tier, and environment-by-environment level to create a more secure enviroment.

## [Capturing Security Requirements through Misuse Cases](./pdfs/Capturing%20Security%20Requirements%20through%20Misuse%20Cases.pdf)


-  Name: Just like normal use cases, every misuse case should have a distinguishing name.
- Summary: One or two sentences should describe the interaction performed.
- Author: Whoever wrote the misuse case.
- Date: When it was written.
-  Basic path: This will be the normal path of action taken, ending with success for the misuser and thus failure for the system and its owners.