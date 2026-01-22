# Ex. 1 - Rating Vulnerabilities
## Compare risk management and vulnerability assessment.

Risk managment is made in the planning and design phase, made to think of pottential threads and design preventive measures.

Vunerability assesment is used when a system is up and running, made to analyse problems that are found on the existing system and how much they will impact the system and organization as a whole

# Ex. 2 - Common Vulnerability Scoring System (CVSS)
## a) Name the four groups that make up the CVSS.

1. Base metrics
2. Temporal metrics 
3. Enviromental metrics
4. Suplemental metrics

## b) For each group, explain the given metrics. If there are different kinds of metrics, you should also explain those.

### 1. Base

#### Exploitability

##### 1. Attack vector

    (P) Physical
    (L) Local only
    (A) Adjacent network 
    (N) Network

##### 2. Attack Complexity

    (H) High
    (L) Low

##### 3. Priviledge Required

    (H) High
    (L) Low
    (N) None

##### 4. User Interaction

    (R) Required
    (N) Not Required

#### Impact

##### 1. Confidentiality

    (H) High
    (L) Low
    (N) None

##### 2. Integrity

    (H) High
    (L) Low
    (N) None

##### 3. Availability

    (H) High
    (L) Low
    (N) None

#### Scope

##### 1. Scope

    (C) Changed - The vulnerable and impacted component are the same
    (U) Unchanged - The vulnerable and impacted component are not the same

### 2. Temporal metrics 

#### Exploit Code Maturity

    (U) Unproven, entirely theoretical exploit
    (POC) Proof-of-concept exists out there, no known maliciously used exploits
    (F) Functional exploit is available
    (H) Functional Exploit is widely disseminated
    (X) Not defined (skip this part of the metric)

#### Remediation Level

    (O) Official Fix is available
    (TF) Temporary fix is available
    (W) Workaround is available Unofficial, non-vendor patches Temporary change in configuration
    (U) Nothing is released yet
    (X) Not defined

#### Report Confidence

    (U) Unconfirmed by the source, or there are multiple conflicting reports
    (R) Significant details are published e.g. proof-of-concept
    (C) Confirmed by the source
    (ND) Not defined

### 3. Enviromental metrics

#### Modified Base Metrics
What is the impact of the enviroment around the system Z.b. Loss of life, enviromental impact, physical assets, etc.

    (H) High
    (M) Medium
    (L) Low
    (N) None
    (ND) Not defined

#### Security Requirements

##### 1. Confidentiality

    (H) High
    (M) Medium
    (L) Low
    (ND) Not defined

##### 2. Integrity

    (H) High
    (M) Medium
    (L) Low
    (ND) Not defined

##### 3. Availability

    (H) High
    (M) Medium
    (L) Low
    (ND) Not defined


### 4. Suplemental metrics

##### Safety (S)
Whether exploitation could impact human safety

##### Automatable (AU)
Can exploitation be automated at scale?

##### Recovery (R)
How difficult system recovery is after exploitation

##### Value Density (V)
How much valuable data is concentrated in the affected system

##### Response Effort (RE)
Effort required to respond and remediate

## c) Now that you have gotten a better insight into the CVSS, you can look up a calculator for it online. Think of an attack and choose the fitting metrics for it. To better compare your results, note down the link of your calculator and your result.

https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator

https://www.first.org/cvss/calculator/3-0


# Ex. 3 - Vulnerability of the Day -  