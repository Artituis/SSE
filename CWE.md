In this file I pretend to list Common Weakness Enumeration (CWE) entries and note possible mitigations that can be implemented in a software development enviroment.

[CWE-242: Use of Inherently Dangerous Function](https://cwe.mitre.org/data/definitions/242.html)

Mitigation: Static analysis of code, to not alow the use of Inherently Dangerous Function. Automatically reject Pull requests with bad functions.

[CWE-272: Least Privilege Violation](https://cwe.mitre.org/data/definitions/272.html)

Could be implemented by devOps in a automated way, by running the processes with different users.

Access to ouside systems also need to be taken into acount. Ex: root access to a external database, can lead to exposure of data.

 		
[CWE-258: Empty Password in Configuration File](https://cwe.mitre.org/data/definitions/258.html)

Should also be a concern of the devops team.

[CWE-256: Plaintext Storage of a Password](https://cwe.mitre.org/data/definitions/256.html)

Resolved by salting passwords

[CWE-260: Password in Configuration File](https://cwe.mitre.org/data/definitions/260.html)

How can this be solved? As it can be stored in a string inside of the binary, leading the passoword to be easily accesible by static analysis.
Would setting the password as a enviroment variable be more secure? But what if a actor or unauthorized person has access to the enviroment the system is running on, could they then have acces to the passwords?