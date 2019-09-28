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
- University of California, Berkeley
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

## What happened in GA, 2018?

+ Lead-up to the election was fraught:
    - allegations that Secretary of State Kemp tried to suppress Black voters
    - a history of insecure election data
    - a lawsuit to require paper ballots over the standard DRE voting machines

+ The 2018 election produced anomalous results that could have been caused by malfunctioning, misprogrammed, or hacked election technology, including DREs

---

## GA has a long history of voter suppression

+ Voting Rights Act (1965) 
    - Prevents racial discrimination in voting
    - Section 5 required certain states to get "preclearance" before changing voting procedures that might affect minority voters

+ Shelby County v. Holder (2013) overturned the preclearance rule
    - Since then, election officials in Georgia have closed nearly 8% of the state's polling places

+ SoS Kemp's "exact match" law: requires name on voter registration application to exactly match the legal name
    - Any discrepancy renders the registration "pending".
    - In 2018, 53,000 voter registrations were pending. 70% were from Black voters.

---

## Help America Vote Act (HAVA) and DREs

+ HAVA passed in 2002 in response to serious problems with punchcard voting machines in the 2000 election
    - Gave states funding to upgrade from punchcard and lever systems, among other requirements
    - Many states used funding to purchase touchscreen DREs

+ Premier (later ES&S) is the DRE provider in Georgia
    - Evidence that the company had strong ties to the Republican party and state officials

+ The AccuVote-TSx machines were shown to have significant problems
    - elaborate


---

## Kennesaw State

+ Contractor for GA to program voting machines, house their voter registration database, etc.
    - Director, Merle King, notable apologist for DREs

+ 2017: Logan Lamb discovered he could access Kennesaw State's Center for Election server, with critical election data (voter records, passwords, etc.) 
    - entire voter registration database for the state of Georgia, including sensitive personal information
    -  instructional PDFs with pass- words for poll workers to sign into a central server on Election Day
    - software files for the state’s ExpressPoll pollbooks
    - Lamb could have altered data, preventing some voters from voting

---

## Curling et al. v. Kemp, 2016-2018

+ Lawsuit was seen in court just months before the 2018 election
    - Pointed to Kennesaw State's poor security and history of issues with DREs

+ Curious behavior
    - Wiped the Kennesaw State servers, the only potential source of forensic evidence

+ SoS Kemp ran against Stacey Abrams for Governor
    - Kemp was SoS overseeing the election; didn't recuse himself
    - Voter suppression continued: closed polling places, signature rejections, exact match law, etc.


---

## Coalition for Good Governance (CGG) Suit, 2018

+ Focuses on Lt. Gov contest

+ Novel argument: "SoS doesn't conduct elections"
    - programs/configures the machines (previously subcontracted to Kennesaw)
    - collects & reports the results (subcontracted to Clarity/Scytl)
    
+ Novel argument: "kill the messenger"
    - Plaintiffs and Dem party told SoS about breaches/vulnerabilities; SoS accused them of hacking

---

## Anomalous results

+ High undervote rate, much higher than down-ticket contests

+ Undervote rate varied substantially by mode of voting
    - Higher rate for ballots cast on DREs
    - Higher in precincts with larger percentage of Black voters

+ Evidence of unusual DRE behavior, using data from poll tapes in Winterville Train Depot precinct

---

## Differential Undervote Rate in Lt. Gov Contest

+ Hypothesis: the undervote rate in the Lt. Governor contest was significantly higher for DRE votes than for paper (absentee by mail) votes

+ Statistical test: assume that the number of undervotes in each contest is fixed, but randomly distributed across modes of voting (hypergeometric)

+ Data: reported vote totals by county and mode of voting, publically available from GA SoS website

---

## Differential Undervote Rate in Lt. Gov Contest

Contest			|  Counties w significant disparities |
:---------------|------------------------------------:|
Lt. Governor 					| 101 |
Secretary of State 				| 4  |
Attorney General				| 4 |
Commissioner of Agriculture		| 5 |
Commissioner of Insurance		| 4 |
State School Superintendent		| 5 |
Commissioner of Labor			| 2 |
Public Service Commission District 3 | 4 |
Public Service Commission District 5 | 4 |

---

## Differential Undervote Rates and Black Voters

+ Data: precinct-level reported vote totals and voter registration in Fulton County

+ Hypothesis: the differential undervote rate by mode of voting in the Lt. Governor contest was significantly higher in precincts with a larger proportion of registered Black voters

+ Permutation test: 
    - under the null, the differential undervote rate is independent of race
    - randomly permute differential undervote rate and compute correlation with percentage of registered Black voters by precinct

---

## Differential Undervote Rates and Black Voters


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

---

## Winterville Train Depot (SoS Kemp's precinct)

+ Citizen photographed poll tapes (total votes cast for each candidate on each machine) after precinct closed 

+ Primarily Democratic (D) precinct; 6 of 7 DREs showed majority votes D
    - Machine 3 showed majority votes for R in every contest
    - What are the chances?

+ Permutation test: no parametric assumptions, no assumptions about voter preferences
    - Assume voters were directed to machines at random
    - Condition on the total number of votes per machine + total number of votes for each candidate
    - Simulate distributing votes across machines

---

## Winterville Train Depot (SoS Kemp's precinct)

Contest					        | $p$-value | $p$-value if machine 3 were flipped|
|:------------------------------|------------:|---------:|
Governor						| 0.114      | 0.464 |
Lt. Governor 					| 0.025       | 0.795 |
Secretary of State 				| 0.018       | 0.450 |
Attorney General				| 0.151       | 0.543 |
Commissioner of Agriculture		| 0.026       | 0.734 |
Commissioner of Insurance		| 0.030       | 0.604 |
State School Superintendent.    | 0.097       | 0.807 |
Commissioner of Labor			| 0.008       | 0.797 |
Public Service Commission District 3 | 0.046  | 0.280 |
Public Service Commission District 5 | 0.025  | 0.939 |

---

## Conclusions

+ Statistical anomalies suggest that DREs failed to record a large percentage of votes in the Lt. Governor contest

+ Evidence that some DREs malfunctioned in the election -- Winterville Train Depot is an example of potential "vote flipping"

+ GA lawmakers are poised to replace DREs with BMDs for all voters

