---
layout: ../../layouts/MdPostDescLayout.astro
title: 'Notes on Prior Authorization (PA)'
LastUpdatedDate: 2024-04-05
CreatedDate: 2024-03-01
description: 'Main PA page'
author: 'Jeff'
tags: []


---
* [Link to consolidated stats, video notes, etc.](/posts/67-stats/)
* [Link to competition](/posts/69-competitors/)

## 4/17/2024
### Various process flows with and without Quick Qual
1. Easy path
	* patient visits doctor
1. PA needed, immediate approval on first PA attempt
	* patient visits doctor
1. Most annoying. PA needed, missed an exam or other item on checklist
	* patient visits doctor
1. We solve the problem with Quick Qual
	* patient visits doctor
1. We solve the problem with PCL Payer Coverage Letter
	* patient visits doctor
1. We solve the problem with Insurance Portal RPA
	* patient visits doctor



## 3/26/2024

### Competitive Research
* Cerner/Oracle ; DrChrono ; Forbes
* Jan 2023 [blog post](https://blogs.oracle.com/healthcare/post/the-prior-authorization-process-what-makes-it-painful-and-how-to-improve-it)
* Oct 2023 [blog post](https://drchrono.com/blog/2023/10/electronic-prior-authorization-why-your-practice-needs-this-technology-now/)
* Sept 2023 [Forbes article](https://www.forbes.com/sites/sethjoseph/2023/09/27/ai-and-standards-arent-enough-fixing-prior-authorization-will-require-something-else-entirely/?sh=76c5583c6993) that AI and Standards aren't sufficient to solve PA


### Info on RCM from Availity
* Availity bought some of Olive's PA business see below. j
* [Revenue Cycle Management 101](https://www.availity.com/blog/2023/december/back-to-basics-healthcare-revenue-cycle-management-101) published 12/21/2023 
* Text:
	1. RCM – it’s an acronym that’s thrown around a lot in healthcare circles. 
	1. It is a critical component to any healthcare organization, as well as an omnipresent process that touches many hands, from front desk schedulers all the way to C-suite executives. 
	1. Many may be familiar with the term, but what does it really mean? 
	1. Let’s break it down. 
	1. At its core, revenue cycle management, commonly known as RCM, centers on – you guessed it – a healthcare organization’s revenue cycle. 
	1. Weaving through many sections of healthcare operations, the revenue cycle encompasses various moving parts: patient registration, claims submission, and denials and appeals, to name a few. 
	1. On their own, these areas are no doubt important. 
	1. However, when collectively viewed through the lens of the overall revenue cycle, they are vital to success. 
	1. For an organization’s revenue cycle to run on all cylinders, these varied forces must work together – and work properly – to create a high-functioning revenue cycle. 
	1. If patient care delivery is seen as the center of healthcare, revenue cycle is its cornerstone. 
	1. Care outcomes are of course of the utmost importance, but when healthcare operations are examined from the business side, a different perspective emerges 
	1. Business executives and those with a hand in the management of the revenue cycle at a health system must also be invested in the things like coding accuracy and the technology used to ensure the organization’s payment portals function properly. 
	1. This is because a core function of the business side of healthcare s optimizing the revenue cycle, and these duties are key pieces of the puzzle. 
	1. Imagine the revenue cycle as an assembly line: each task must be checked off the figurative list in order to see a finished product. 
	1. These various moving parts must work together to achieve the desired outcome. 
	1. Take eligibility, for example. 
	1. Verifying coverage is crucial for determining patient eligibility. 
	1. If a patient’s insurance provider has changed and they fail to mention this, or if a manual error mistakenly notes the wrong policy number, consequences could arise for the patient, provider, and payer. 
	1. This task, along with the other, are critical cogs in the wheel of the overall revenue cycle. 
	1. While many pieces can function independently, the true strength comes from working together. 
	1. To perfect care delivery, these behind-the-scenes elements have to be in optimal working order. 
	1. The importance of RCM lies in its ability to streamline and enhance the financial workflow, ensuring accurate and timely reimbursement for the services provided. 
	1. Efficient RCM practices help minimize revenue leakage, reduce billing errors, and enhance cash flow, which, in turn, allows healthcare providers to allocate resources effectively and focus on delivering high-quality patient care. 
	1. Moreover, in an era of complex healthcare regulations and evolving payment models, a robust RCM strategy becomes even more crucial to navigate the intricacies of the billing and reimbursement landscape, ultimately contributing to the overall financial viability of healthcare organizations. 
	1. For hospitals and physician practices to succeed, a spotlight needs to be placed on the revenue cycle, and RCM measures need to be enacted to optimize operational processes and meet revenue goals. 
	1. And perhaps most importantly, with a high-functioning revenue cycle in place, the patient support side of healthcare to able to thrive. Learn how Essentials Pro from Availity can help manage your RCM here.
 

### Notes on [Medscape article](https://www.medscape.com/viewarticle/997446?form=fpf)
* Date published: October 17, 2023
* About New England Baptist Hospital (NEBH) in Boston
* 100 orthopedic surgeons on staff
* NEBH has been using software for about 5 years (since 2018?). 
	* Software has reduced write-offs by 30%, staff cosgs by 25%.
	* PA requests used to take 11 days; now take 3 days.
	* 'This software not only saves staff time, but it can also more accurately predict when prior authorization is needed,' said director of patient access Lidiya Hadzhieva
* So far, the software is mainly used at large organizations like hospital systems. **But as word gets out and the software becomes easier to use, private practices and other smaller entities may join the automation trend.**
* Usual AMA report stats: 16 hours per week on PA; 60% of doctors say it's hard to know when PA is needed; 93% of doctors reported care delays.
* Experts estimate that 80% of PA work can be automated, but most practices still use phone/fax even as PA burden continues to increase
* Automation software connects directly to the EHR (electronic health record) of each practice. 'When the doctor places an order in the EHR, the process starts automatically,' Hadzhieva said. 'The doctor may not even notice it.'
	* although this automatic connection can be used, a lot of the software products also allow access via fax, phone, and the web portal of the payer.
* Manually keeping track of payer rules is very time-consuming, but automation uses bots to visit each payer site to look for rules changes. 
* **One vender, Infinitus, uses a voice-based bot called Eva that calls up each payer and speaks with a representative.**
#### section of medscape article on Olive Software
1. "Automatically updating payer rules is not a new technology," said YiDing Yu, MD, chief product officer at Olive, the automation vendor for New England Baptist. 
1. "What is new in the last 5 years is extracting the information needed for the prior authorization out of the clinical notes."
1. This is challenging because each doctor has different ways to describe each step of clinical work. 
1. To identify this shorthand, **Yu said Olive uses NLP**.
1. Yu asserts that Olive is actually better than a practice's staff at digging out clinical information. 
1. **She said staff without much clinical training may miss terms that the software can catch, and they don't have the time to go back many months into the record to find valuable information.** But automation can do that.
1. At NEBH, *the software is used mainly by physicians in fairly small private practices who are on staff.* 
#### Cost, pricing, and GTM for software
1. **They are using the software on the hospital's dime, but it only works inside the hospital, Hadzhieva said.**
1. For their work outside of the hospital, they would have to purchase the Olive software on their own, she said.
1. Despite the promising outcomes for products like Olive, *automation software is still primarily used by large organizations.* 
1. Vendors say very few private practices have bought it yet. 
1. "The technology works, but it is still in the early-adopter phase," Yu said. 
1. For one thing, the software can be expensive. Very few venders reveal their prices, but Yu did so. 
1. She said **Olive normally costs about $50,000 a year for even a small organization.** She insisted, however, that the savings from avoiding just one denial each month for a hip surgery would justify the expense.
#### comparison between SureScripts and Olive
1. Surescripts and Olive have entirely separate functions. 
1. Yu said **Olive is limited to procedures** [aka does not cover prescriptions], 
1. so it benefits specialties like oncology, neurosurgery, colorectal surgery, vascular surgery, and cardiology. Olive does not cover prescriptions, because they operate on a different technology.
#### Other hurdles
1. Yu said another hurdle for adopting the software is the kind of EHR systems that doctors use. At this point, only a few EHR systems — such as Epic, Cerner, and Athena — are compatible with Olive. Large organizations tend to use Epic and Cerner, while many practices often use Athena or a variety of other systems, she said. Despite stunted demand, there is no shortage of companies offering automation software for medical (ie, non-prescription) prior authorization. One compilation lists 25 such vendors, including companies like Myndshft, Rhyme, Infinitus, Infinx, and Waystar. As with any start-up technology, companies occasionally buy out each other.
1.  In addition to issues like cost, specialty, and EHR compatibility, another hurdle is that few doctors even know the technology exists. Vendors say marketing focuses on larger provider organizations, not smaller practices. 
1. Even many tech-savvy doctors, like Adam Bruggeman, MD, an orthopedist and CEO of Texas Spine Care Center in San Antonio, say they know little about the technology. 
1. **"There is definitely a need to automate prior authorization," he said. "But I don't know of any colleagues who use it." He has only just begun to explore vendors, he said.**
1. *Many medical practice consultants also have not yet explored the technology.*
1. "Automation makes a lot of sense, because there are a lot of repetitive tasks in prior authorization," said Jill Arena, CEO of Portland, Oregon-based Health e Practices. 
1. "But I haven't looked into it yet and **none of my clients has even asked about it.**" "I could see how it could be an easier sell for large organizations," she added. "They have an IT person and a CFO who can explore the issue. Smaller practices usually don't have that kind of expertise."

#### Next
1. Until now, need to buy 2 different PA products: one for prescriptions, another for procedures.
1. This has to do with incompatible electronic transmission standards, which are used to digitize information, said Susan Lawson-Dawson, content marketing strategist for the vendor Myndshft Health.
Myndshft has long been selling automation software for medical prior authorizations, but now it is introducing a product for prescriptions, Lawson-Dawson said. She said Myndshft will then be the only vendor to automate both kinds of prior authorizations. 
1. Lawson-Dawson said Myndshft has 685 customers to date and is looking for more business. 
1. Recently the company entered the Google Cloud Marketplace. 
1. Google Cloud customers can now direct their committed spend with Google to purchasing Myndshft, meaning they could get it at a discount. 
1. Software like Olive and Myndshft can operate independently of payers, but a vendor called Rhyme depends on payers for its software to function, said Rhyme CEO Joe Anstine. 
1. He said more than 300 payers have agreed to install the Rhyme system, and Rhyme has signed up a number of large health systems to use the product. 
1. Initially, he said, clinicians paid for the service, but now Rhyme is beginning to find payers to foot the costs and to let clinicians use it for free, which would open Rhyme up to smaller practices. 
1. EHR companies themselves are beginning to offer automation, too. 
1. Epic, for example, has created a tool for prior authorization as part of its Epic Payer Platform. 
1. Like Rhyme, it requires payer cooperation, because information goes back and forth between clinician and payer in what is called bi-directional exchange. 
1. The Epic product is still in its pilot phase. 
1. Epic reported that several large health systems were using its product in conjunction with a specific payer — for instance, Mayo Clinic with Blue Cross and Blue Shield of Minnesota and Ochsner Health with Humana. 
1. According to Epic, the arrangement reduced Mayo's denials due to additional documentation requests by 63% for professional billing. 
1. Automating with just one payer still means the clinician has to deal with manual processes at other payers. 
1. But a large clinician could have sufficient volume with that one payer to make the arrangement useful.

### Payers and PA
1. Ultimately, *payers may take the automation business away from vendors, offering a free product to all clinicians.*
1. **But don't hold your breath.** Payers first have to rebuild their electronic systems to accommodate an electronic connection with providers. Even then, some payers might hold back from automating, forcing practices to continue manually processing some prior authorizations.
1. Efforts are underway, however, to mandate payers to support prior authorization automation. For this to happen, payers would have to revamp their data so that it could be easily read by practices' EHRs. This would mean adopting a specific interoperability standard called Health Level 7 Fast Healthcare Interoperability Resources (FHIR). Toward this goal, the Centers for Medicare & Medicaid Services proposes to require payers to adopt FHIR by January 2026. (CMS still has to finalize the rule.) Experts say the two-year ramp-up time is needed because it takes extensive work for payers to translate their data into FHIR.
#### Regence Payer + MultiCare CC Provider
1. The only payer to switch so far is Regence in WA state, which has a pilot with just one provider, an ACO (accontable care organization) called MultiCare Connected Care.
	* Anna Taylor, VP at MultiCare CC, said these doctors have been "enthusiastic" about the arrangement.
1. The results of the pilot are impressive. 
1. Taylor said **automation has resulted in a 233% productivity gain for MultiCare clinicians, and 89% of submissions to Regence get an immediate response.**
1. There is a **potential downside**, however, to working directly with payers. 
1. *A direct connection to clinicians allows payers to access the doctor's clinical notes, which could make many doctors uneasy.*
1. Taylor said two of the 27 other payers that MultiCare works with are "highly interested," but **it would take a lot of work for them to get connected with practices and other clinicians.** 
1. Ultimately, payers could offer automation and third-party vendors might then fade away. 
1. However, physicians may resist working directly with payers if the arrangement requires full access to their medical records.


### other notes on olive software
* Interesting divestment of AI-enabled utilization mgt article from [April 2023](https://www.fiercehealthcare.com/health-tech/availity-picks-olive-ais-prior-authorization-business-automation-startup-sheds-business). Sold it to Availity
	* Olive pulled in a $400m round from Vista Equity Partners at a $4b valuation
	* Olive has a raised a total of $902m since company founded in 2012.
	* Olive had aquired PA AI vendor Verata Health.
* CEO Sean Lane said at the time that Olive was experiencing many of the same headwinds as other organizations—including shifts in the industry landscape, evolving customer expectations and challenging market conditions—but also acknowledged the company needs to "reconcile missteps" that were made, he wrote.
* The company's market research indicates that **payers and providers collectively spend up to $13 billion every year managing an administrative process widely blamed for care delays, patient dissatisfaction, staff burnout and friction between payers and providers, executives said in a press release. To date, automation of authorizations has been difficult because they require both administrative and clinical data, which are often stored in siloed information systems and in non-standardized formats that require manual intervention to bring together. Availity’s AI auth solution leverages automation capabilities and natural language processing (NLP) to streamline authorizations workflow. The tech can import and structure payers’ medical policies to automatically approve authorizations based on the codified medical policies and front-end capabilities enable providers to simplify authorizations workflow, according to the company. The use of automation and NLP also helps automate and standardize clinical data collection, eliminating the multiple steps and handoffs in a manual workflow, and can reduce authorization approval time from days to seconds, executives said.

### Pretty interesting Olive / Verata m&a announcement from 2020
* [Link to press release](https://www.prnewswire.com/news-releases/olive-acquires-verata-health-to-accelerate-artificial-intelligence-technology-for-healthcare-providers-and-payers-301185294.html)
* Verata CEO was a former MD at Mayo Clinic. Quote:
	* *"Caring for patients at Mayo Clinic was life-changing," said Dr. Jeremy Friese, CEO of Verata and former Mayo physician executive. "We started Verata to have an impact on patients and providers across the country. Combining our AI solution with Olive's creates the leading platform to solve prior authorization on **both ends of the fax machine** at providers and payers to drive impact for millions of patients."*


***

## 3/25/2024
### Updated statistics
* [Axios article](https://www.axios.com/2024/01/18/health-insurance-prior-authorization-doctors) on rule change from Jan 2024. 'New limits on PA hailed as good first step'.
* [Axios article](https://www.axios.com/2023/01/27/states-target-doctor-authorization) on 'States jumping into PA fight' from **January 2023**
* [Medscape article](https://www.medscape.com/viewarticle/997446?form=fpf) on vendors, providers, and payers trying to automate PA. Reference to Rhyme / PriorAuthNow 

***

## 3/24/2024
* Podcasts with Athena / Devoted Health founders
* Ed Park and Todd Park co-interviewed in late 2023 at a16z Las Vegas LP summit. [Link](https://a16z.simplecast.com/episodes/devoting-your-life-to-reinventing-a-broken-system-cftMcIms)
	* **Date aired:** March 25, 2024
	* **Title:** Devoting Your Life to Reinventing a Broken SystemO
	* **Summary:** In this episode, a16z General Partner Vijay Pande chats with Ed and Todd Park, the visionary siblings behind Devoted Health. Their mission? To overhaul a healthcare system they describe as critically essential yet deeply flawed. The Park brothers delve into the genesis of their ambition to construct a healthcare system from scratch, underscoring the sector's urgent need for technological innovation and the game-changing role of AI. Kicking off with an American dream story, this episode is a must-listen for anyone interested in how technology can reshape healthcare for the better.
	* 12:45 - After 25 years of learning the hard way, we've realized that the way to do this is to build a complete alternative universe healthcare-system-as-a-service in order to hyperscaale that set of results everywhere.
	* 13:00 - People call us a tech-enabled virtual Kaiser Permanente, or a 'tech-enabled pay-vider' aka portmanteau of payer and provider. We call it an all-in-one healthcare solution. 
	* 13:20 - We built from scratch five ingredients: 
		1. Built an entire insurance company.
		1. Navigator service. Health-enabled concierge service called HealthGuide. 'I don't care how smart you are; you can't navigate through the complex system'
		1. Partner with great local doctors and hospitals. For a whole bunch of historical reasons, overfitted on emergency reactive service. Not for preventive care 
		1. Full-scale in-house medical group. The first truly great virtual care for seniors. 95% is delivered telemedically
		1. Key to entire thing. Software called Orinoco. Ultra-modern... the first end-to-end software that can run both payer and provider operations. From thousands of sources, gets the right care at the right time.
	* Coordinates all these complex pieces 'stitch in time to save nine'.
	* We feel like we've split the atom. 
	* NPS of 77. Higher than Apple, Starbucks. Way higher than legacy healthcare systems.
	* 5 star clinical outcomes, that our own clinicians can't believe
	* Cuts the cost of medicare (and primary and preventative care)
	* Fastest growing health insurance provider in America.
	* Started in 8 counties in FL with 2300 members in 2019. Now serve 140,000 members in 13 states.
	* 17:45 Medicare Advantage market. Outsourced private medical care for seniors. $425B market, growing to $1T by 2035.
		* We're starting with seniors, but aim is to do it serve everyone.
		* Getting calls from other countries. No one else can build Orinoco.
	* 19:00 Double click on why Ed Park is the one of the best engineers on the planet and no software person understands the healthcare system the way he does.
		* Ed was the First developer for Orinoco. 
		* Todd in 8th grade said I'm going to be the best big brother I can.
* [Michael Lewis 2022 interview](https://overcast.fm/+5Jd4rkhMI) with Todd Park and Bob Gatewood.
	* **Date Aired:** April 5, 2022
	* 'Season 3, Episode 1: Six Levels Down'

***

## 3/19/2024
### Links from Christin
1. Physician specialties varied widely in rates of services that required prior authorization, with highest rates among radiation oncologists (97%), cardiologists (93%), and radiologists (91%) and lowest rates among pathologists (2%) and psychiatrists (4%).
	* [Source](https://jamanetwork.com/journals/jama-health-forum/fullarticle/2780396)
1. The most common treatments subject to PA. Raw notes here. See Slack and /stats page for cleaner formatting...
* Seymour also created this [ChatGPT answer on PA in the context of Emergency Medicine](https://docs.google.com/document/d/1A_GQCyJ0Sfpaqm7kcnoA-mnPj48Oojy56nuMvgbHqik/edit?usp=sharing) accessible via primary gmail account.

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
* p. 6, '12% of total denials attributed to bad prior authorizations'.
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
