[comment]: # (
Compile with make %.slides.pdf
) 

---
title: "Election Integrity and Electronic Voting Machines in 2018 Georgia, USA"
subtitle: |
          | E-Vote-ID 2019
          | Bregenz, Austria
author: 
- Kellie Ottoboni
- Philip B. Stark
- Vanessa Teague
institute: 
- Pinterest
- University of California, Berkeley
- University of Melbourne
date:  1--5 October 2019
classoption: "aspectratio=169"
theme: metropolis
colortheme: owl
themeoptions: background=dark 
header-includes:
    - \setbeamercolor{title separator}{fg=green}
    - \setbeamercolor{progress bar in section page}{fg=green}

---

**Kellie and Philip are very grateful to Vanessa for giving this talk!**

---


## GA has a long history of voter suppression

+ Voting Rights Act (1965) 

. . .

+


. . .

+
---

## HAVA and DREs

---

## Kennesaw State

+ Contractor for GA to program voting machines, etc.
+ Director, Merle King, notable apologist for DREs

---

## Logan Lamb

+ Discovered Kennesaw State's Center for Election server had critical election data (voter records, passwords, etc.) 

---

## VR Database


---

## Curling et al. Suit, 2016 (Coalition for Good Governance)

Abrams v. Kemp for Gov.

Kemp was SoS; didn't recuse himself

Closed polling places; signature rejections; etc.

---

## CGG Suit, 2018

+ Focuses on Lt. Gov contest

+ Novel argument: "SoS doesn't conduct elections"
    - programs/configures the machines (previously subcontracted to Kennesaw)
    - collects & reports the results (subcontracted to Clarity/Scytl)
    
+ Novel argument: "kill the messenger"
    - Plaintiffs and Dem party told SoS about breaches/vulnerabilities; SoS accused them of hacking
    
+ Curious behavior
    - Wiped the Kennesaw State servers, the only potential source of forensic evidence

---

## Anomalous results

+ High undervote rate, Much higher than down-ticket contests

+ Undervote rate varied substantially by mode of voting

    - Higher rate for ballots cast on DREs
    - Higher in precincts with larger percentage of Black voters

---

## Differential Undervote Rate in Lt. Gov Contest

Contest			|  Counties w significant disparities |
:---------------|------------------------------------:|
Lt. Governor 					| 101 |
Secretary of State 				| 4  |
Attorney General				| 4 \\
Commissioner of Agriculture		| 5 \\
Commissioner of Insurance		| 4 \\
State School Superintendent		| 5 \\
Commissioner of Labor			| 2 \\
Public Service Commission District 3 | 4 |
Public Service Commission District 5 | 4 |

---

Permutation test: no parametric assumptions, no assumptions about voter preferences


---

## Winterville Train Depot (SoS Kemp's precinct)

Contest					        | correlation | $p$-value |
|:------------------------------|------------:|---------:|
Governor						| -0.134      | 0.9903 |
Lt. Governor 					| 0.557       | 0.0001 |
Secretary of State 				| 0.092       | 0.0582 |
Attorney General				| 0.078       | 0.0902 |
Commissioner of Agriculture		| 0.207       | 0.0003 |
Commissioner of Insurance		| 0.246       | 0.0001 |
State School Superintendent.    | 0.154       | 0.0050 |
Commissioner of Labor			| 0.041       | 0.2376 |
Public Service Commission District 3 | 0.042  | 0.2329 |
Public Service Commission District 5 | 0.125  | 0.0145 |





