---
layout: ../../layouts/MdPostDescLayout.astro
title: 'Notes on Prior Authorization (PA)'
LastUpdatedDate: 2024-04-05
CreatedDate: 2024-03-01
description: 'main log'
author: 'Jeff'
tags: []


---
* [Link to video / deck notes](/posts/67-pitch/)


## 3/25/2024
### Updated statistics
* [Axios article](https://www.axios.com/2024/01/18/health-insurance-prior-authorization-doctors) on rule change from Jan 2024. 'New limits on PA hailed as good first step'.
* [Axios article](https://www.axios.com/2023/01/27/states-target-doctor-authorization) on 'States jumping into PA fight'
* [Medscape article](https://www.medscape.com/viewarticle/997446?form=fpf) on vendors, providers, and payers trying to automate PA. Reference to Rhyme / PriorAuthNow 

### Notes from Justin on Wed 3/20/2024
* Roland's new company [HealthHelp](https://www.healthhelp.com/benefits-management-offerings/)
* Sequoia-funded company **Co:Helm**, the co-pilot for healthcare. See [post announcing their funding](https://www.sequoiacap.com/article/partnering-with-cohelm-the-co-pilot-for-health-care/). Abdel Mahmoud and Zahid Mahmoud are cofounders.
* **Basys.ai** [Smart Prior Auth and Utilization Mgt](https://www.basys.ai)
	* [TC article](https://techcrunch.com/2023/08/10/basys-ai-2-4m-prior-authorization-mayo-clinic-healthcare/): 'Basys.ai grabs $2.4M for its prior authorization tech powered by Mayo Clinic’s data'. from August 2023.i
		* 'And the administrative costs associated account for between 20% and 34% of U.S. healthcare expenditures.'
		* Basys combines generative AI and deep learning to power its “engine,” which can automate up to 90% of the prior authorization requests for drugs and procedures at high accuracy, Nigam told TechCrunch. The platform also doesn’t require sensitive data from insurance companies or doctors, thus reducing the typical integration time from up to a year down to weeks.
		* “The engine is trained on extensive Joslin Diabetes Center and Mayo Clinic’s longitudinal data of more than 10 million patients,” Nigam said. “This translates to flattening the cost curve for patients and reducing administrative burden by leveraging AI.”
		* In addition, by automating the encoding of payer policies, Basys can more quickly plot timelines with health plans at a rate of up to nine months faster than most of its competitors, of which Nigam said included companies like Cohere Health.
		* The company makes its commercial launch today, buoyed by $2.4 million pre-seed funding. Nina Capital led the round and was joined by a group of investors, including Eli Lilly (Lilly Ventures), Mayo Clinic, Two Lanterns Venture Partners, Asset Management Ventures and Chaac Ventures.
		* Basys initially began selling to providers and had been bringing in revenue, but has since pivoted its business model to selling to health insurance companies. It is now initiating pilots with two large payers in Massachusetts and Minnesota, Nigam said.
		* The company is also working on capturing patient outcomes through reducing readmission rates and determining if the progression of the patient’s disease has stopped or slowed down.
		* “We also make sure we have a lot of information about the patients,” Nigam said. “Sometimes when you make decisions, it is not entirely based on one or two attributes; it’s based on hundreds or thousands of attributes along with the understanding of the insurance company’s policies. Once you match these policies with the patient information, then resolving a prior authorization request is more nuanced.”
* [Cohere Health](https://coherehealth.com)
	* Cohere Health, which leverages artificial intelligence to streamline prior authorization for health plans and risk-bearing providers, raised 550 million to meet growing demand. The company grew from less than 10 employees in 2020 to more than 700 employees today, now serving five health plans, processing 5.5 million prior authorizations annually for more than 15 million health plan members and 420,000 healthcare providers nationally. (PR Newswire)
* [Rhyme](https://www.getrhyme.com) is rebrand of early company PriorAuthNow
* **Itilit Health** * Itiliti Health, a 2.5-year-old, Eden Prairie, Mn.-based healthcare-focused whose software helps manage prior authorizations for payers, has raised $2 million in funding co-led by Bread and Butter Ventures and Altitude Ventures. Other backers in the round include M25, SpringTime VC, and Groove Capital. 
	* website: https://itilitihealth.com
	* from their site: 'A better way to prior-authorize. Itiliti Health’s best-in-class technology leverages AI and automation to accelerate communication between payers and providers, creating a touchless prior authorization solution that applies the right medical policies while helping to automate prior authorizations quickly, securely and cost-effectively.'


## 3/19/2024
### Links from Christin
1. Physician specialties varied widely in rates of services that required prior authorization, with highest rates among radiation oncologists (97%), cardiologists (93%), and radiologists (91%) and lowest rates among pathologists (2%) and psychiatrists (4%).
	* [Source](https://jamanetwork.com/journals/jama-health-forum/fullarticle/2780396)
1. The most common treatments subject to PA:
	* Genetic testing: 100 percent
	* Specialty drugs: 100 percent
	* Elective inpatient surgical services: 92 percent
	* Election inpatient medical services: 88 percent
	* High cost non-specialty prescription drugs: 88 percent
	* High-tech imaging: 88 percent
		* Chloe: for advanced imaging, serious issue
	* Post acute care facility services: 88 percent
	* Cardiology: 80 percent
	* Durable medical equipment: 80 percent
	* Orthopedics: 80 percent
	* [Source](https://www.beckerspayer.com/payer/most-common-treatments-subject-to-prior-authorization.html)
1. Medscape surveyed 17,461 U.S. clinicians representing more than 30 specialties. Rate of claim denials and resubmissions by specialty.
	1. Plastic surgery: 28 percent
	2. Emergency medicine: 22 percent
		* Chloe: yes, this is true and painful. Some of this is handled through decision tree
		* Seymour: ChatGPT answer
	3. Radiology: 20 percent
	4. Critical care: 20 percent
	5. General surgery: 19 percent
	6. Physical medicine and rehabilitation: 19 percent
	7. Anesthesiology: 19 per
	* To get full report, create free account. [Source](https://www.beckersasc.com/asc-coding-billing-and-collections/which-physicians-have-the-most-claims-denied-resubmitted-a-specialty-breakdown.html).
* For general surgeons, 19 percent of claims are denied or need resubmitted, according to Medscape's "Physician Compensation Report 2020."


***
## 3/13/2024
* Article on pain of PA suggested by Chloe preoius week 3/07
* See [this AMA article](https://www.ama-assn.org/practice-management/prior-authorization/what-doctors-wish-patients-knew-about-prior-authorization) from Christin on pains of PA with Dr. Resneck


***
## 3/06/2024

### Change Healthcare Whitepaper: PA automation, interoperability, etc.
* Title: 'Automation and Interoperability: Innovating Prior Authorization to Improve the Patient Experience'
* [Link to PDF in Box](https://app.box.com/s/7dbomegx2lvrivkqcrqhez8bwijxe78x)
* On Page 4, in the bullet on *Coverage Requirements Discovery (CRD)*:
	1. Currently, a lack of consistency and transparency around payer requirements increases providers’ chances of missing a required authorization or requesting authorization for the wrong procedure at the outset. 
	1. As **80% of authorization requests require extra work, rework, or manual follow-ups**, getting this first step right can be crucial to expediting the authorization. 
* p. 6, '12% of total denaisl attributed to bad prior authorizations'.
* p. 7, Automating Medical Necessity Review. Among benefits, 'get immediate approval or deferred decision within native workflow, **elminating need to call or fax** payer'
	1. Hospital case managers and patient-access staff can stay within their workflows to conduct medical necessity reviews and submit authorization requests directly through their EMR and care management systems, which will automatically direct the needed information—including the medical review—to the correct payer system. 
	1. That’s just one piece of the prior authorization puzzle solved (albeit the most challenging). 
	1. Today, we can automate even more of the process using the now-ubiquitous EHR. 
	1. **Almost all information needed to process a prior authorization request can be found in the EHR automatically via software.** 
	1. *If that information can be extracted and applied to criteria without human intervention, the approval determination is further accelerated.* 
	1. **Once the prior authorization request is entered, nothing more needs to be done until the request is approved or pended.** 
	1. *And given that many initial pended decisions are due to a lack of information found in the medical record, retrieving data directly from that record will likely increase the number of approvals.*
	1. That solution is currently live at an expanding number of customer sites. 
	1. Hospital admissions using these capabilities can automatically populate the medical necessity review and then transmit it to the correct payer. 
	1. Using transparent, automated reviews that include embedded EHR data can also increase trust with payers.




***

### National Health Expenditure for US (NHE)
* Source: [Centers for Medicare and Medicaid Services](https://www.cms.gov/data-research/statistics-trends-and-reports/national-health-expenditure-data/nhe-fact-sheet)
* NHE grew 4.1% to $4.5 trillion in 2022, or $13,493 per person, and accounted for 17.3% of Gross Domestic Product (GDP).
* Medicare spending grew 5.9% to $944.3 billion in 2022, or 21 percent of total NHE.
* Medicaid spending grew 9.6% to $805.7 billion in 2022, or 18 percent of total NHE.
* Private health insurance spending grew 5.9% to $1,289.8 billion in 2022, or 29 percent of total NHE.
* Out of pocket spending grew 6.6% to $471.4 billion in 2022, or 11 percent of total NHE.
* Other Third Party Payers and Programs and Public Health Activity spending declined 10.2% in 2022 to $564.0 billion, or 13 percent of total NHE.
* **Hospital expenditures grew 2.2% to $1,355.0 billion in 2022**, slower than the 4.5% growth in 2021.
* Physician and clinical services expenditures grew 2.7% to **$884.9 billion in 2022**, slower growth than the 5.3% in 2021.
* Prescription drug spending increased 8.4% to **$405.9 billion in 2022**, faster than the 6.8% growth in 2021.


***
### Remington Report

* The truth is although prior authorizations has been an issue among healthcare providers for many years, little is known about the cost, either to individual practices or the healthcare system as a whole. 
* In 2009, one study estimated that on average, prior authorization requests consumed about **20 hours a week per medical practice**: 
	1. **1 hour** of the doctor’s time, 
	1. **~2 hours** of clerical time, 
	1. **13 hours** of nurses’ time.
* A study by Health Affairs further revealed that when the time is converted to dollars, practices spent an average of *$68,274 per physician per year interacting with health plans*. 
* **This equates to $23 billion and $31 billion annually!** 
* Prior authorization ultimately ends up costing the health care system more than it saves.


***

### 2019 Report by NIHCR 
* by National Institute For Health Care Reform
* [Link to PDF](https://www.nihcr.org/wp-content/uploads/Altarum-Prior-Authorization-Review-November-2019.pdf)
* Authors: Ani Turner, George Miller, Samantha Clark
* From footnote 5: American Medical Association. 2016 AMA Prior Authorization Physician Survey. 2016. https://www.ama- assn.org/sites/ama-assn.org/files/corp/media-browser/public/government/advocacy/2016-pa-survey- results.pdf. Published 2017. Accessed July 25, 2019.
	* Reference to footnote 5 is on page 6 of PDF: 'Physicians have reported that, overall, **72% of PA requests are approved on initial request and an additional 7% are approved on appeal**. <sup>5</sup> 
* PAs are typically only valid for a specified length of time, after which additional requests must be submitted for continued prescription refills or therapies.
#### Notes on NIHCR funding
* Funding by Altarum Institute Center for Sustainable Health Spending
* The National Institute for Health Care Reform is a 501(c)(3) nonprofit, nonpartisan organization established by the International Union, UAW; Chrysler Group LLC; Ford Motor Company; and General Motors to conduct health policy research and analysis to improve the organization, financing and delivery of health care in the United States.
* From 2009 through 2013, the Institute contracted with the Center for Studying Health System Change (HSC) to conduct health policy research and policy analyses under the direction of HSC President Paul B. Ginsburg, PhD. Beginning in 2014, NIHCR has funded Altarum Institute’s Center for Sustainable Health Spending (CSHS), the Detroit Community-Academic Urban Research Center (Detroit URC), and the Urban Institute to conduct research and policy analyses with an emphasis on research to improve health in Detroit.






***

## 3/05/2023

1. **How many patient visits per year?**
	* From [2023 Commonwealth Fund report](https://www.commonwealthfund.org/publications/issue-briefs/2023/jan/us-health-care-global-perspective-2022), about 4 visits per patients per year as of 2022.
	* multiplied by 330m people in the US in 2022, 330m * 4 = *1.32 billion patient visits per year.*
1. **How many prior auth requests?**
	* From [Wikipedia](https://en.wikipedia.org/wiki/Physicians_in_the_United_States) there are ~1m doctors in the US. Probably about 990,000. That number fits with 3 doctors per 1000 people, 301 doctors per 100,000 people. 330m * 0.3% = 990k doctors in the US.
	* combining 990k doctors * 41 prior auths generated per week per physician (from AKASA report) = 40.6m prior auths generated per week.
	* 40m prior auths requests * 52 weeks = *2 billion prior auth requests per year.*
	* this means that *there about 1.5 prior auth requests per doctor visit*. 
1. **what percentage of prior auth requests get denied?**
	* Unclear. According to [KFF 2021](https://www.kff.org/medicare/issue-brief/over-35-million-prior-authorization-requests-were-submitted-to-medicare-advantage-plans-in-2021/), about 5% of prior auths are denied, but that only samples from Medicare Part B.
		* If we use the 5% number, that means that 100m denials of prior auth requests per year.
1. **Cost impact**
1. **Care impact**

### 2022 AMA Survey on PA (Prior Authorization) Infographic #1
* [Link to infographic PDF](https://www.ama-assn.org/system/files/prior-authorization-survey.pdf)
* 'For those patients whose treatment requires PA, how often does this process delay access to necessary care?' **94% report delays**.
* ' How often do issues related to the PA process lead to patients abandoning their recommended course of treatment?' **80% lead to some abandonment**.

### 2022 AMA Survey on PA (Prior Authorization) Infographic #2
1. [Link to infographic PDF](https://www.ama-assn.org/system/files/prior-authorization-reform-progress-update.pdf)
1. Increase in number of PA requirements from 2018-2022
	* For prescription medications, 81% of physicians report that the number of PAs has increased in the last 5 years.
	* For medical services, 80% of physicians report that the number of PAs has increased in the last 5 years.
1. 64% and 61% (for prescription medication and medical services, respectively) of physicians report that it is somewhat or extremely difficult to determine whether prescription or med service require PA.
1. Continuity of patient care. **89% of physicians** report that PA interferes with continuity of care.
1. Physicians report **phone** as the most commonly used method for completing PAs. 
	* Moreover, *only 29% of physicians report that their EHR* system offers electronic PA for prescription medications.
	* *Table of usage* Phone (54%,56%); Fax (47%,45%); EMR/PMS (52%,33%); Plan portal (40%,40%); Email or US Mail (24%,26%). 


### New sources on number of prior authorization requests per year
* the below sources are not ideal
	1. This KFF source (aka Kaiser Health News) draws data only from Medicare Advantage in 2021. 
		* [Headline](https://www.kff.org/medicare/issue-brief/over-35-million-prior-authorization-requests-were-submitted-to-medicare-advantage-plans-in-2021/#:~:text=Just%20over%202%20million%20prior,or%20in%20part%20in%202021): 'Over 35 Million Prior Authorization Requests Were Submitted to Medicare Advantage Plans in 2021' of which 2 million were fully or partially denied.
		* 2m / 35m =  5% of all prior auths have been denied
	1. This [JAMA article from 2021](https://jamanetwork.com/journals/jama-health-forum/fullarticle/2780396) only examines Medicare Part B.
		* 'This cross-sectional study examined medical services paid for by government-administered Medicare Part B, which lacks prior authorization requirements, for approximately **6.5 million beneficiaries**; **2.2 services per beneficiary per year** would have been subject to prior authorization under the coverage rules of a large Medicare Advantage insurer, and these services accounted for 25% of annual Part B spending.'

### AKASA report from May 2023
* [Link](https://akasa.com/blog/prior-authorization-trends/)
* According to AKASA research, submitting and checking the status of a prior authorization request takes *12 minutes and 7 seconds**.
* With **41 prior authorizations per physician per week**, it’s no surprise that 88% of physicians say the burden associated with prior authorizations is “high” or “extremely high.”

### 2022 Crowe Report 
* [Link to PDF](https://www.crowe.com/-/media/crowe/llp/widen-media-files-folder/h/hospital-double-whammy-less-cash-in-more-cash-out-chc2305-001b.pdf)
* Title: 'Hospital double whammy: Less cash in, more cash out Increasingly frugal payors and high inflation add up to a big financial headache for hospitals and health systems'
* From pg 7, denial rate for these providers sampled by Crowe LLP public accounting firm. Increased from 10.2% in early 2021 to 11% by 2022. I don't like this b/c the monthly chart on pg 7 tells a different story. 1.5 - 2.0% per month...how does that add up to 10% per year? It doesn't.

***

Sources

* 1/24/2024 - ['Advocacy in action: Fixing prior authorization'](https://www.ama-assn.org/practice-management/prior-authorization/advocacy-action-fixing-prior-authorization)
* 1/19/2023 - ['Health systems plagued by payer-takeback schemes, 110,000 denials'](https://www.ama-assn.org/practice-management/prior-authorization/health-systems-plagued-payer-takeback-schemes-110000)
* 4/4/2023 - ['17 fast facts on prior authorization'](https://www.beckersasc.com/asc-news/17-fast-facts-on-prior-authorization.html)
* 10/13/2022 - ['Prior authorization largest regulatory burden for group practices: survey'](https://www.beckersasc.com/asc-coding-billing-and-collections/prior-authorization-largest-regulatory-burden-for-group-practices-survey.html)
	* Eighty-two percent of group practice executives say prior authorization is very or extremely burdensome, according to the Medical Group Management Association's "Annual Regulatory Burden Report."
* 2020? [Prior Authorizations: The Saga Continues For Providers](https://remingtonreport.com/intelligence-resources/futurefocus/prior-authorizations-the-saga-continues-for-providers/) data from 2019.
	* The average number of hours per week for physician spent was 4.6. The average number of hours per week for their staff was 11.6.

***

From the AMA report:
Prior authorization’s financial impact
“Prior-authorization denials on inpatient accounts are a key driver behind the dollar value of denials increasing to 2.5% of gross revenue in August 2022 from 1.5% of gross revenue in January 2021,” the report says. “That’s an increase of 67%.”

***

A couple more numbers from that same source: A study by Health Affairs further revealed that when the time is converted to dollars, practices spent an average of $68,274 per physician per year interacting with health plans. This equates to $23 billion and $31 billion annually! Prior authorization ultimately ends up costing the health care system more than it saves.

***

A fantastic number to have would be X patient visits per year -> lead to Y prior auth requests -> Of which Z get initially denied......(translated to some $ number in cost impact)
