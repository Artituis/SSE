# Ex. 1 - Defensive Coding

## a) How is defensive coding different from risk analysis and secure design?

While risk analysis is about domain threats, priotization of critical problems, what could go wrong and  secure design is about minimizing risk, principle of least privilege and attack vectors, defensive coding is about creating code that is secure, that uses security components the proper way, and is a lot more related to the programing and architecture side.

## b) What are the defensive coding principle?

REVIEW THIS

Writing insecure code is surprisingly easy
• Mysterious coding assumptions
• Many different technologies to know
🔧 Maintainability still counts
• Duplicate code is even harder to secure
• Vulnerabilities often have regressions and incomplete fixes
📚 Know your APIs!
• Misusing an API in the wrong context can be a vulnerability
e.g. an XML parser that also executes includes
• Copying from Internet examples without understanding? For shame.
🎭 Don’t be paranoid
• Know what you can trust, but don’t trust StackOverflow or ChatGPT blindly
23


The principles of defensive coding are 

### - Input Handling

Validate and Sanitize

### - Error and Information Control
Handle Exeptions

[CWE-209: Generation of Error Message Containing Sensitive Information](https://cwe.mitre.org/data/definitions/209.html)

Mitigations:

Handeling exeptions internaly.
Making sure a debugging error is not returned to the user.
Handeling errors close to the source.
If necessary and possible, configure error messages to be less verbose, there fore returning less information.

Possible real world implementation:

Log the error in a private database and just give the user a unique error code that can then be analized by a support technitian.

### - Object Lifecycle Security
    Class Inheritance, Imutability, Cloning

Making sure that a critical class and class functions cannot be extended. (Using the `final` key word for example)

Prefer that classes are imutable.

Create own way of clonning a class. Built in ways of cloning objects are insecure.

Cloning allows a class to be instatiated without the constructor.

This also relates to serializable objects **"Deserializing is essentially constructing objects without executing constructors"**

### - State Managment
### - Data Protection
### - Boundary Control

# Ex. 2 - Complexity

## Explain the following statement: "Complexity is the enemy of security” (– Gary McGraw)

A complex code is more difficult to debug, to test, and to understand. These factors make the chances of a security flaw or a logic flaw to be much higher. 

Ciclomatic complexity and architechtural complexity makes

# Ex. 3 - Control flow graph



TODO: STUDY HOW TO DO THIS GRAPH BY HAND

The Formula: M = E - N + 2P
• E = Edges (arrows in the graph)
• N = Nodes (boxes/diamonds in the graph)
• P = Connected components (usually 1)

Lines of Code:
267
Nodes:
139
Edges/Branches:
176
Decision Points:
38
Return Statements:
8
Parameters:
1

E = 176
N = 139
P = 1?

M = 179 - 139 + 2 = 42 

This is high risk and cannot be fully tested.

# Ex. 4 - Vulnerability of the Day - Server-Side Request Forgery


[VMware vCenter Server updates address remote code execution vulnerability in the vSphere Client ](https://www.cve.org/CVERecord?id=CVE-2021-21973)



# Notes

## Defensive conding principles

- Writing insecure code is easy
    With misterious code assumptions 