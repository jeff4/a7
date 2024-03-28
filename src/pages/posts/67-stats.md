---

layout: ../../layouts/MdPostDescLayout.astro
title: 'Statistics, video outline, etc.'
LastUpdatedDate: 2024-04-16
CreatedDate: 2024-03-06
description: 'n/a'
author: 'Jeff'
tags: []


---
* [Main PA page](/posts/68-temp/)
* [Competitors](/posts/69-competitors/)

## Consolidated statistics
* Jeff's estimates
	* 2 billion PA requests a year, calculated from number of physician visits
	* Total US NHE in 2022 is $4.5 T. [Source: CMS](https://www.cms.gov/data-research/statistics-trends-and-reports/national-health-expenditure-data/nhe-fact-sheet)
	* $1.3T is the part of the NHE that JH thinks might be subject to PA. Sum of two items: $885B (Physician and clinical services) + $405B (prescription drug spending)
* From NYT video
	1. Dr. Shikha Jain, oncologist at 1:30: PA impacts every insured person in this country. According to CMS, that's about 92% of the US population, aka 300m Americans.
	1. Dr. Jessica Korman, Gastroerontologist: When prescribing meds, 95% of the time, i need to go through PA (around 1:55)
	1. After a PA is denied, there may be appeal or pay out of pocket (OOP), but **80% of the time**, treatment is simply abandoned. (3:40)
	1. Might have peer to peers as much as 5-10 times a day
	1. For Dr. JKorman's practice, they have 4 fulltime employees whose sole focus is obtaining PAs for medications. (4:45)
	1. (4:58) **USA spends bout $35B a year on administrative costs of PA.**
		* Note that [this Fierce Health article on Olive](https://www.fiercehealthcare.com/health-tech/availity-picks-olive-ais-prior-authorization-business-automation-startup-sheds-business) says Olive company research indicates that $13B a year is spent managing PA. See main PA page for more on that article and relevant quote
		* December 2020 [press release](https://www.prnewswire.com/news-releases/olive-acquires-verata-health-to-accelerate-artificial-intelligence-technology-for-healthcare-providers-and-payers-301185294.html) by Olive on acquiring Verata for AI tech says PA costs $31B a year.
* Axios article on US states increasing regulatory scrutiny on PA from Jan 27, 2023
	* Refers to [Crowe research Nov 2022 article](https://www.crowe.com/-/media/crowe/llp/widen-media-files-folder/h/hospital-double-whammy-less-cash-in-more-cash-out-chc2305-001b.pdf) saying that **dollar value of insurer coverage denials increased by 67% between January 2021 to August 2022**.
* Medscape article
	1. AMA stats -- See infographic sections below
		* 16 hours per week on PA; 60% of doctors say it's hard to know when PA is needed; 93% of doctors reported care delays.
	1. Experts estimate that 80% of PA work can be automated, but most practices still use phone/fax even as PA burden continues to increase


### 2022 AMA Survey on PA (Prior Authorization) Infographic #1
* [Link to infographic PDF](https://www.ama-assn.org/system/files/prior-authorization-survey.pdf)
* 'For those patients whose treatment requires PA, how often does this process delay access to necessary care?' **94% report delays**.
* ' How often do issues related to the PA process lead to patients abandoning their recommended course of treatment?' **80% lead to some abandonment**.

### 2022 AMA Survey on PA (Prior Authorization) Infographic #2
1. [Link to infographic PDF](https://www.ama-assn.org/system/files/prior-authorization-reform-progress-update.pdf)
1. 64% and 61% (for prescription medication and medical services, respectively) of physicians report that it is somewhat or extremely difficult to determine whether prescription or med service require PA.
1. Continuity of patient care. **89% of physicians** report that PA interferes with continuity of care.
1. Physicians report **phone** as the most commonly used method for completing PAs. 
	* Moreover, *only 29% of physicians report that their EHR* system offers electronic PA for prescription medications.
	* *Table of usage* Phone (54%,56%); Fax (47%,45%); EMR/PMS (52%,33%); Plan portal (40%,40%); Email or US Mail (24%,26%). 

### From Change Healthcare whitepaper
* As **80% of authorization requests require extra work, rework, or manual follow-ups**, getting this first step right can be crucial to expediting the authorization. 
* **12% of total denials attributed to bad prior authorizations** (p. 6)
* *Automation and Interoperability: Innovating Prior Authorization to Improve the Patient Experience*
* [Link to PDF in Box](https://app.box.com/s/7dbomegx2lvrivkqcrqhez8bwijxe78x)


## Rates of PA by specialty, procedure, likelihood of denial/resubmissions
1. **Prior Auth requirement rates by specialty.** [Source](https://jamanetwork.com/journals/jama-health-forum/fullarticle/2780396).
	* *Specialties with highest PA rates:*
		1. Radiation oncologists: 97%
		1. Cardiologists: 93%
		1. Radiologists: 91%
	* *Specialties with lowest PA rates:*
		1. Pathologists: 2%
		1. Psychiatrists: 4%
1. **The most common treatments subject to PA.** [Source](https://www.beckerspayer.com/payer/most-common-treatments-subject-to-prior-authorization.html).
	1. Genetic testing: 100%
	1. Specialty drugs: 100%
	1. Elective inpatient surgical services: 92%
	1. Election inpatient medical services: 88%
	1. High cost non-specialty prescription drugs: 88%
	1. High-tech imaging: 88%
	1. Post acute care facility services: 88%
	1. Cardiology: 80%
	1. Durable medical equipment: 80%
	1. Orthopedics: 80%
1. **Rate of claim denials and resubmissions by specialty.** Medscape surveyed 17,461 U.S. clinicians representing more than 30 specialties. [Source](https://www.beckersasc.com/asc-coding-billing-and-collections/which-physicians-have-the-most-claims-denied-resubmitted-a-specialty-breakdown.html). (*To get full report, create free account at Becker.*) 
	1. Plastic surgery: 28%
	2. Emergency medicine: 22%
	3. Radiology: 20%
	4. Critical care: 20%
	5. General surgery: 19%
	6. Physical medicine and rehabilitation: 19%
	7. Anesthesiology: 19%
* Stats shared by Christin on 3/19/2024



## 3/19/2024
* Gift link to [NYT video](https://www.nytimes.com/2024/03/14/opinion/health-insurance-prior-authorization.html?unlocked_article_code=1.c00.sJL6.W6MlRzmi_cXu&smid=url-share)
* Video posted at NYT on 2024-03-14.

### Notes
* mp4 file, 8:37 long
* 0:00 - 0:14 about patient who goes blind b/c of PA delays. Doctor says "Call me to defend why you think this patient needs this." Is what the Payer tells the referring PCP, forcing them to justify referall to specalist.
* 0:19 - 0:25 Multiple sclerosis case
	* v-o: Without warning, the insurance company stops your medications
	* Doctor: No you cannot give this drug
	* v-o: So you become paralyzed 
* 0:26 - 0:47
	* v-o: Imagine your father has cancer. His doctor orders an MRI
	* Doctor: No you cannot order this imaging. Have you considered using this cheaper cancer drug?
	* v-o: Insurance company causes delay after delay 
	* Doctor: You don't need this surgery
	* v-o: He dies. [camera close-up on woman wiping away tears]
* 0:47
	* NYTimes Opinion Title Card
* 0:57
	* v-o: An absurd process has infiltrated American healthcare. It's called Prior Authorization. Here's how it works. Before a doctor provides a treatment, your insurance requires them to prove it's necessary. This is often a time-consuming process that can cause dangerous delays.
* 1:05 - 1:16
	* Doc: I'm sorry, your cancer could be cured but we need to wait for the insurance company to approve your chemotherapy.
* 1:18 - 1:42
	* Introduces Dr. Shikha Jain, Oncologist
	* v-o: She's barricaded by PA daily.  
	* Dr. Jain: This is a really big issue (1:22 - 1:25)
	* **And it impacts every single person in this country who has insurance**. 
	* v-o: PA was actually created to save you money. Decades ago, it was used sparingly [graphic shows timeline moving from late 1970s to 1980]. Only to make sure that expensive treatments, like long hospital stays were absolutely necessary.
	* v-o: But now...
* 1:46 - 2:10
	* Dr. Jain: ..it's devolved into a system where a lot of times things are really denied for no reason. Even everyday medications now require insurance approval.
	* Doc 2: It could be for medications to treat heartburn
	* Docs 3-4: It could be med...It could be test strips to test blood sugar
	* Dr. Jain: ...chemotherapy..
	* More docs: ...Prozac...
	* Doc: when i prescribe a medication, I'd say that 95% of the [NYT graphic of large 95% number] time, I need to obtain a prior authorization
* 2:11 - 2:32 
	* v-o: NYT Opinion interviewed more than 50 doctors and patients. Their experiences suggest that insurance companies often weaponize this mundane process in order to control doctors and inflate their profits.
	* Doc 2 or 3?: If they deny care or delay care, that's money the insurance company gets to keep
	* Doc 4: The way they profit is to deny care.
* 2:33 - 2:40
	* v-o: As PA has spread, delays in care have become normalized...and so have tragedies.
	* images of various organs, hearts, procedures, surgeries, etc.
* 2:41
	* v-o: One in three doctors say it's caused a serious medical issue or even the death of one of their patients.
* 2:48 - 2:58
	* Focuse on patient named Ocean who went blind
	* Ocean: It was like the insurance company telling me that my life didn't matter.
* 2:59 - 3:07
	* Focus on patient Michael Trotman, MS patient
	* v-o: Michael couldn't walk or stand for 4 months.
	* Michael: And it's like, I am scared of MS. But my fear as of right now is right now is actually the insurance company.
* 3:08 - 3:29
	* Focus on patient Vivian Gonzales
	* v-o: Vivian lost her father to cancer.
	* Vivian: I spent so much time on the phone, writing letters, faxing...[long pause]...I didn't get to spend that time with my father.
	* v-o: This is medical injustice disguised as paperwork. 
* 3:31
	* Photos of PA denials.
	* Screen goes to black with just white text: Your request was denied.
* 3:35 - 4:29
	* When you PA is denied, you have three options
1. **Pay out of pocket.** v-o: But healthcare is so ridiculously expensive, that that's not really realistic.
1. **Abandon Treatment.** v-o: You can give up. That's what happens up to 80% of the time. A *win* for your insurance company.
1. **Appeal.** v-o: Or your doctor can go to bat for you. (3:54) 
	* Pediatrician: When our PAs get denied, we have to do what's called a peer-to-peer. 
	* Dr. Jain: A p2p is supposed to be a phone call where you call somebody [at the insurance company] to justify the care you want to deliver.
	* Ped: I'm a pediatrician and sometimes I'll end up talking to a neurologist
	* Dr. Jain: People who couldn't pronounce the names of the drugs I was trying to prescribe.
	* Ped: Oftentimes, it's not even a physician. 
	* Dr. Jain: Now imagine you need to do that 5-10 times a day.
	* Other doc: What's even more ridiculous about this whole process is that after we go through all of this is that after we go through all this--if you're really a determined provider, you'll probably get your drug or your procedure authorized.
* 4:30 - 4:57
	* Gastroerontologist, Dr. Jessica Korman: Insurance companies say that this process helps reduce the cost of expensive treatments, ensure member safety, and lower the total cost of care. But what it's actually doing is creating a lot of expensive bureacracy. 
	* Dr. JKorman: We have 4 full-time employees who their sole focus is on obtaining PAs for medications to treat Crohn's disease and ulcerative colitis...and that's just for *one* disease state!
* 4:58 - 5:19
	* v-o: By one estimate, the US spends about $35B a year on the administrative costs of PA. 
		* Source: 'Active Steps to Reduce Administrative Spending Associated with Financial Transactions in US Health Care.'
	* Dr. JKorman: These resources could be devoted to patient care, answering phones in a timely fashion. I might actually get to go home and see my family on a regular basis.
* 5:20 - 5:37
	* v-o: In an admission of sorts, some companies have actually pledged to reduce prior authorizations. But those efforts only scratch the surface.
	* Dr. JKorman: I am a board-certified Gastroenterologist. I know what I'm doing, only being blockaded by all of this bureaucracy, red tape, which really only serves to enrich the insurance companies.
* 5:38 - 5:51 Insurance Co profits in 2023
	* Cigna - $5.2B; Elevance - $6B; United Healthcare made $22B
* 5:52 - 6:23
	* Dr. Jain: I had a patient who had a new diagnosis of lymphoma and the insurance company was giving me a hard time to give me chemotherapy. I got someone on the phone and I told the person, I said, 'I need your name. B/c when this young man dies, I want to tell his parents who was the reason behind it.'
	* Dr. Jain: I went home and cried after I hung up the phone because I was so emotionally exhausted. **And that was just *one* patient.**
	* Dr. J: I had seen **25 other patients** that day. And many of them would eventually need PAs as well.
* 6:24
	* v-o: PA gives your insurance company more power than your doctor. 
	* v-o: Now, there are some complicated cases when it makes sense to double check that your doctor isn't unnecessarily overprescribing. Imagine you've had a cancerous tumor removed. To be extra safe, your doctor recommends an additional treatment but it costs $170k, 
	* Sara: On the one hand, i can see where insurance companies are coming from with wanting to take a careful look at these expensive treatments. On the other hand, I'm a human and I'm a young mom. What's my life worth?
	* v-o: Sara's insurance denied the treatment. The question is, do you think they made that decision based on what was her best interest, or theirs [payer's best interest]?
	* v-o: In many countries, these tough ethical decisions about what is covered is made by governments, not for-profit insurance companies
* 7:26
	* v-o: The government should abolish PA or at the very least, reform it.
	* Image of Republican Senator Curt VanderWall. Sen VW: My goal with Senate Bill No. 247 is to reform the PA process
* 7:38 - 7:56: Gold Carding
	* Texas House Bill 3459 image. PA streamlining process known as 'gold carding'.
	* v-o: A handful of states have created gold card programs: Arkansas, Louisana, Michigan, Texas, West Virgina. Pilot program in Vermont.
	* In other words, doctors who have previously successfully obtained PA approvals are exempt from needing them again.
	* All states and the Federal Gov't should pass laws like these.
* 7:57
	* v-o: Your insurance should not be a barrier between you and the health care you need.
* 8:05 - 8:30
	* Ocean: I finally got the PA to see the neuro-ophthalmologist after 12 weeks. And he said, 'We're going to do this surgery but it's only to preserve the vision that you have left. If we had seen you earlier, that would have been a different story'
	* Ocean: Maybe I'd be able to see now. Maybe I'd have a different life. 


***
