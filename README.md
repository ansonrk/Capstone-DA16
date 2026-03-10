# TRANSPLANT EQUITY IN THE UNITED STATES
**NASHVILLE SOFTWARE SCHOOL**
**COHORT DA16**
**AUTHOR: RICHARD ANSON**

# Overview
This capstone project examines equity in access to heart, kidney, and lung transplants in the United States. Although organ transplantation is a life‑saving intervention, access to evaluation, waitlisting, and receipt of organs is not equally distributed across populations. This project aims to identify disparities in transplant access and outcomes based on demographic, socioeconomic, and geographic factors.

# Project Motivation
This topic is deeply personal. My son underwent a heart transplant, giving me firsthand insight into the urgency, complexity, and emotional weight of accessing life-saving transplant care. Navigating the transplant process revealed how factors beyond clinical need—such as location, socioeconomic resources, and systemic barriers—can significantly influence patient outcomes. This experience strengthened my commitment to using data analytics to examine inequities in transplant access and to support fairer, more inclusive healthcare decision-making.


# Primary Question
* Are there measurable disparities in access to heart, kidney, and lung transplants in the United States based on demographic, socioeconomic, and geographic factors?

# Supporting Questions
* Do transplant rates differ by race, ethnicity, sex, or age?
* Are there differences in wait times across demographic or geographic groups?
* How does insurance status or region relate to the likelihood of receiving a transplant?
* Are outcome measures (e.g., transplant rates or mortality while waiting) unevenly distributed?


# Data Sources
* UNOS/OPTN: waitlist burden, long-wait shares, candidate wait-time buckets, transplant totals
* U.S. Census: population denominators + socioeconomic context
* CDC mortality: regional mortality background measures

# Files used
* data/uno_waitlist.csv
* data/Cand+reg_Organ_by_Waiting._Time.csv
* data/uno_transplant.csv
* data/census_cleaned.csv
* data/CDC_MORTALITY_cleaned_joined_long.csv

# Key Definitions
* Registration: one listing on a waiting list. A person may have multiple registrations (multiple centers and/or multiple organs).
* Candidate: one unique patient (counted once, even if multiple listings/organs).
* Waitlist burden (per 100k): waitlisted / population × 100,000.
* Long-wait share (≥ 1 year): percent of waitlisted candidates/registrations waiting at least one year.
* Crude mortality rate: overall population death rate (used here as regional context; not waitlist-specific mortality).


# Data preparation
* Clean numeric fields (commas, percents, missing values)
* Harmonize geography (state/region labels; state abbreviations for mapping)
* Forward-fill organ labels in grouped bucket tables
* Reshape wait-time buckets (wide → long) and compute long-wait share (≥1 year)

# Analysis
* Compare waitlist burden per 100k by organ × region/state
* Compare long-wait share (≥1 year) by organ × region
* Examine race/ethnicity wait-time bucket patterns using candidate buckets
* Use uninsured, income, and crude mortality as ecological context indicators

# Key Findings
* Access burden is not evenly distributed: Kidney shows the highest waitlist burden per 100k and the highest long-wait share (≥1 year). 
*	Region matters: Long-wait shares vary across Northeast, the Midwest, the South, and the West; the South tends to be higher on heart burden and social risk context. 
*	Demographic differences are visible: Race/ethnicity groups show different exposure to waits ≥1 year; patterns differ by organ. 
*	Geography is concentrated: A small set of states accounts for the highest per-capita waitlist burden, especially for the kidney. 

# Tools
*	Python for cleaning, analysis, and chart generation
*	Power BI for dashboard-style visuals and maps
*	Excel
*	PowerPoint for presentation

# Conclusion
The data support the conclusion that transplant access is unevenly distributed across geography, organ type, and candidate subgroups — but the strongest evidence here is about disparity patterns, not causal drivers.









