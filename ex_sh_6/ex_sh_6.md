# Ex. 1 - Code Quality and Security Practices
## a) Explain what a code smell is and why it matters for security. Give two examples and their corresponding refactorings.

Code smells are patterns of code that make it less readable, and harder to understand. It affects security because it makes the code harder to read, therefore harder to find possible bug, or logic problems. 

Examples are: nested if statements, that could be decoupled or serialized, for a clearer control flow understanding; long functions, that could be decoupled into smaller, more readable funcions; and poor naming, be it of variables, functions or classes, that might need more time or thinking of the names.

## b) Describe the Test-Driven Development (TDD) cycle. Is there a security benefit of writing tests before implementation?

TDD makes the tests be a priority. It requires that all the tests be writen first, acording to the expecific requirements. Then all the code written is made to fit the tests, leading to a 100% code coverage by tests.

More detailed description?

The security benefits of TDD, is to describe an expected behaviour, that makes possible logical problems in the code that might make it behave in a unexpected way. It makes it easier to refactor, and to alter maiking it easier to detect if something is broken. 

## c) Why is using printf(str) instead of printf("%s", str) a vulnerability? How can we exploit it?

Depending on how the printf function is written it can lead to a user exploiting a "CWE-78: Improper Neutralization of Special Elements used OS Command". This can be used maliciously to get information on memory address, and potentially change control flow and code execution.

# Ex. 2 - Static Analysis

## a) Explain the difference between false positives and false negatives. Which one is more dangerous from a security perspective, and why?

False positives is when testing for some adverse effect it is detected, but it is not actually present. A false negative is when the adverse effect is present but is not detected. 

False negatives are more dangerous to security, because it makes bugs or problems not be detected leaving a system vulnerable, without the user, or organization knowing. But false positives can lead to developers not trusting the tools, leading to the developers more probable to leave code vulnerabilities.

## b) What are the four core elements of taint analysis in SAST tools? Briefly describe each.

● Sources: Input that might have malicious or malphormed data (e.g., user inputs, HTTP parameters)
● Sinks: Functions that open an attack vector (e.g., SQL, OS Commands)
● Propagation: Looking where the sources pass inside the code.
● Sanitizer: Funtions that sanitize potential sources.

## c) At which phases of the software development lifecycle can SAST be applied? Give the pros and cons per phase.

In the coding phase SAST can be applyied to the source code. 

Although it can lead to the developers putting to much or to little faith into the Static analysis tools, making the bennefits of static analysis be diminished, if not excluded.

pros
imideate feedback
works with incomplete code

also used in the review phase in the ci cd, it might require aditional loops to fix false positives.

## d) What’s the difference between a linter and full blown static analysis tool?

A linter makes sure that code adheres to certain visual characteristics, making the code have a standard look, making it easier to understand a code base that has multiple developers working on it at once.

STAT will analyse the control/data flow of the code, giving warnings.


# Ex. 3 Alternative 1 - Static Analysis with Semgrep
Use Semgrep to analyze the Log4j library source code (vulnerable version) and understand the benefits and limitations
of static analysis tools. Before doing the task, install semgrep as CLI and VSCode plugin and clone the vulnerable Log4j
version < 2.14.1 from github.
Tasks:
## a) Run Semgrep with the Java security ruleset on the Log4j source code. What are your observations? Explain the potential bugs.
Results in scan_log4j.txt
## b) Examine the vulnerable file directly: JndiLookup.java Identify the dangerous part. Does Semgrep flag this as a vulnerability? Why or why not?
## c) Scan WebGoat. Are Semgrep’s findings legit?
Results in scan_webgoat.txt

# Ex. 3 Alternative 2 - Static Analysis with clang (Hard and Slow)
Clone FFmpeg and checkout a version with a known vulnerability, e.g. n5.1 containing CVE-2022-2566
Tasks:
## a) Scan the vulnerable file with: clang –analyze libavformat/mov.c -I. -I./libavutil. Explain the command. Does the analyzer find anything? Explain.
## b) Now use scan-build configure && make -j$(nproc) from clang to scan the entire project. How many issues did it find? Discuss your observations and results.

# Ex. 4 - Vulnerability of the Day
In the lecture you have talked about uncontrolled format string and OS command injection. Research an example of this
which was not discussed and explain what happened, how it happened and how it was dealt with. In addition to that,
explain which of the CIA properties were affected. (You can look up a CVE, in case you cannot find an attack on a company or something similar.