---
id: kb-03-leave-and-absence
title: "Respellion: Leave and Absence Policies"
description: "Consolidated reference for all leave types at Respellion: holiday/vacation leave (incl. interchangeable holidays), sick leave (incl. Wet Verbetering Poortwachter), parental leave (maternity/partner/parental incl. WAZO), and special leave (study, unpaid, family events, doctor's visits, emergency/short-term/long-term care, informal care)."
category: leave-and-absence
language: en
jurisdiction: NL
audience: [employee]
version: 1.1.0
last_updated: "2026-05-18"
last_source_commit: fb9a84a
topics:
  - holiday-leave
  - vacation-leave
  - sick-leave
  - illness
  - parental-leave
  - maternity-leave
  - paternity-leave
  - partner-leave
  - special-leave
  - study-leave
  - unpaid-leave
  - emergency-leave
  - care-leave
  - mantelzorg
  - interchangeable-holidays
  - reintegration
key_entities:
  legal_frameworks:
    - "Wet Verbetering Poortwachter (WVP)"
    - "Wet Arbeid en Zorg (WAZO)"
    - "Work and Care Act"
    - UWV
  systems_and_tools:
    - Microsoft Shifts
    - Microsoft Teams
    - Exact Online
  roles_and_organizations:
    - People Officer
    - "Health and Safety Provider 'GOED'"
    - Arbodienst
    - Medical Case manager
  leave_types_in_systems:
    - "Verlof (Leave)"
    - "Tijd-voor-tijd (Time-for-time)"
    - "FEESTDAG (interchangeable public holiday)"
  policy_constants:
    - "Full-time vacation entitlement: 25 days (200 hours, 20 statutory + 5 non-statutory)"
    - "Mandatory continuous vacation: 2 consecutive weeks per year"
    - "Carry-over: max 80 hours (full-time)"
    - "Statutory days expire 6 months after accrual year"
    - "Non-statutory supplementary days expire after 5 years"
    - "Interchangeable holidays: 4 per year"
    - "Maternity leave: 16 weeks (20 weeks for multiple births)"
    - "Partner leave: 1 week at 100% + 5 weeks at 70%"
    - "Parental leave: 26 x weekly hours per child under 8"
    - "Paid parental leave: 9 of 26 weeks at 70% before child's 1st birthday"
    - "Wage continuation in illness: 100% year 1, 70% year 2"
    - "Study leave: 5 days/year at 40-hour week (pro rata)"
    - "Doctor's visit: max 2h/visit (4h specialist), 8h/year"
    - "Short-term care leave: max 2x weekly hours/year (e.g. 80h full-time), Respellion pays 100%"
    - "Long-term care leave: 6 weeks/year distributed over 18 weeks, unpaid"
entities:
  - { id: "entity:org/respellion",              type: organization, label: "Respellion" }
  - { id: "entity:org/uwv",                     type: organization, label: "UWV" }
  - { id: "entity:org/goed",                    type: organization, label: "GOED (Health and Safety Provider)" }
  - { id: "entity:org/arbodienst",              type: organization, label: "Arbodienst (occupational health and safety service)", lang: nl }
  - { id: "entity:law/wvp",                     type: law, label: "Wet Verbetering Poortwachter", aliases: ["WVP"], lang: nl }
  - { id: "entity:law/wazo",                    type: law, label: "Wet Arbeid en Zorg", aliases: ["WAZO", "Work and Care Act"], lang: nl }
  - { id: "entity:role/people-officer",         type: role, label: "People Officer" }
  - { id: "entity:role/medical-case-manager",   type: role, label: "Medical Case manager" }
  - { id: "entity:role/request-for-leave",      type: role, label: "Request for Leave role" }
  - { id: "entity:tool/microsoft-shifts",       type: tool, label: "Microsoft Shifts" }
  - { id: "entity:tool/microsoft-teams",        type: tool, label: "Microsoft Teams" }
  - { id: "entity:tool/exact-online",           type: tool, label: "Exact Online" }
  - { id: "entity:leave_type/verlof",                type: leave_type, label: "Verlof (Leave)", lang: nl }
  - { id: "entity:leave_type/tijd-voor-tijd",        type: leave_type, label: "Tijd-voor-tijd (Time-for-time)", lang: nl }
  - { id: "entity:leave_type/feestdag",              type: leave_type, label: "FEESTDAG (interchangeable public holiday)", lang: nl }
  - { id: "entity:leave_type/vacation",              type: leave_type, label: "Vacation leave" }
  - { id: "entity:leave_type/sick",                  type: leave_type, label: "Sick leave" }
  - { id: "entity:leave_type/maternity",             type: leave_type, label: "Maternity leave (Bevallingsverlof)", lang: en, aliases: ["Bevallingsverlof"] }
  - { id: "entity:leave_type/pregnancy",             type: leave_type, label: "Pregnancy leave (Zwangerschapsverlof)", aliases: ["Zwangerschapsverlof"] }
  - { id: "entity:leave_type/partner",               type: leave_type, label: "Partner/Paternity leave (Geboorteverlof)", aliases: ["geboorteverlof"] }
  - { id: "entity:leave_type/additional-partner",    type: leave_type, label: "Additional birth leave (Aanvullend geboorteverlof)", aliases: ["aanvullend geboorteverlof"] }
  - { id: "entity:leave_type/parental",              type: leave_type, label: "Parental leave" }
  - { id: "entity:leave_type/paid-parental",         type: leave_type, label: "Paid parental leave" }
  - { id: "entity:leave_type/unpaid-parental",       type: leave_type, label: "Unpaid parental leave" }
  - { id: "entity:leave_type/adoption-foster",       type: leave_type, label: "Adoption or Foster Care leave" }
  - { id: "entity:leave_type/study",                 type: leave_type, label: "Study leave" }
  - { id: "entity:leave_type/unpaid",                type: leave_type, label: "Unpaid leave" }
  - { id: "entity:leave_type/special",               type: leave_type, label: "Special leave" }
  - { id: "entity:leave_type/emergency",             type: leave_type, label: "Emergency leave" }
  - { id: "entity:leave_type/short-term-care",       type: leave_type, label: "Short-term medical care leave" }
  - { id: "entity:leave_type/long-term-care",        type: leave_type, label: "Long-term care leave" }
  - { id: "entity:leave_type/informal-care",         type: leave_type, label: "Informal care (mantelzorg)", aliases: ["mantelzorg"] }
  - { id: "entity:metric/fte-vacation-days",         type: monetary_constant, label: "Full-time vacation days/year", value: 25, unit: "days" }
  - { id: "entity:metric/fte-vacation-hours",        type: monetary_constant, label: "Full-time vacation hours/year", value: 200, unit: "hours" }
  - { id: "entity:metric/statutory-days",            type: monetary_constant, label: "Statutory vacation days/year (FTE)", value: 20, unit: "days" }
  - { id: "entity:metric/non-statutory-days",        type: monetary_constant, label: "Non-statutory vacation days/year (FTE)", value: 5, unit: "days" }
  - { id: "entity:metric/vacation-carryover-max",    type: monetary_constant, label: "Max vacation carry-over to new year (FTE)", value: 80, unit: "hours" }
  - { id: "entity:metric/interchangeable-holidays",  type: monetary_constant, label: "Interchangeable public holidays per year", value: 4, unit: "days" }
  - { id: "entity:metric/maternity-leave-weeks",     type: monetary_constant, label: "Maternity leave (single birth)", value: 16, unit: "weeks" }
  - { id: "entity:metric/maternity-leave-multi",     type: monetary_constant, label: "Maternity leave (multiple births)", value: 20, unit: "weeks" }
  - { id: "entity:metric/partner-leave-full",        type: monetary_constant, label: "Partner leave fully paid", value: 1, unit: "week" }
  - { id: "entity:metric/partner-leave-additional",  type: monetary_constant, label: "Additional partner leave at 70%", value: 5, unit: "weeks" }
  - { id: "entity:metric/parental-leave-multiplier", type: monetary_constant, label: "Parental leave per child (multiplier × weekly hours)", value: 26, unit: "weeks" }
  - { id: "entity:metric/paid-parental-weeks",       type: monetary_constant, label: "Paid parental leave portion (of 26 weeks)", value: 9, unit: "weeks" }
  - { id: "entity:metric/study-leave-days",          type: monetary_constant, label: "Study leave per year (40h FTE)", value: 5, unit: "days" }
  - { id: "entity:metric/doctor-visit-max",          type: monetary_constant, label: "Reimbursed doctor's visit max per visit", value: 2, unit: "hours" }
  - { id: "entity:metric/specialist-visit-max",      type: monetary_constant, label: "Reimbursed specialist visit max", value: 4, unit: "hours" }
  - { id: "entity:metric/doctor-visit-annual-max",   type: monetary_constant, label: "Doctor's visit annual reimbursement cap", value: 8, unit: "hours" }
  - { id: "entity:metric/short-term-care-fte-max",   type: monetary_constant, label: "Short-term care leave per year (full-time)", value: 80, unit: "hours" }
  - { id: "entity:metric/long-term-care-weeks",      type: monetary_constant, label: "Long-term care leave per year (distributed over 18 weeks)", value: 6, unit: "weeks" }
relations:
  - { s: "entity:org/respellion", p: "complies_with", o: "entity:law/wvp" }
  - { s: "entity:org/respellion", p: "complies_with", o: "entity:law/wazo" }
  - { s: "entity:leave_type/verlof",                p: "registered_in", o: "entity:tool/exact-online" }
  - { s: "entity:leave_type/tijd-voor-tijd",        p: "registered_in", o: "entity:tool/exact-online" }
  - { s: "entity:leave_type/vacation",              p: "requested_in",  o: "entity:tool/microsoft-shifts" }
  - { s: "entity:leave_type/vacation",              p: "approved_by",   o: "entity:role/people-officer" }
  - { s: "entity:leave_type/sick",                  p: "reported_to",   o: "entity:role/people-officer" }
  - { s: "entity:org/respellion",                   p: "wage_continuation_year_1", o: 100, note: "percent" }
  - { s: "entity:org/respellion",                   p: "wage_continuation_year_2", o: 70,  note: "percent" }
  - { s: "entity:leave_type/maternity",             p: "duration",      o: "entity:metric/maternity-leave-weeks" }
  - { s: "entity:leave_type/maternity",             p: "duration_multiple_births", o: "entity:metric/maternity-leave-multi" }
  - { s: "entity:leave_type/maternity",             p: "wage_rate",     o: 100, note: "percent" }
  - { s: "entity:leave_type/partner",               p: "duration",      o: "entity:metric/partner-leave-full" }
  - { s: "entity:leave_type/additional-partner",    p: "duration",      o: "entity:metric/partner-leave-additional" }
  - { s: "entity:leave_type/additional-partner",    p: "wage_rate",     o: 70, note: "percent, paid by UWV up to max daily wage" }
  - { s: "entity:leave_type/additional-partner",    p: "paid_by",       o: "entity:org/uwv" }
  - { s: "entity:leave_type/parental",              p: "entitlement_per_child", o: "entity:metric/parental-leave-multiplier", note: "26 × weekly working hours" }
  - { s: "entity:leave_type/parental",              p: "applies_to_children_under", o: 8, note: "years" }
  - { s: "entity:leave_type/paid-parental",         p: "duration",      o: "entity:metric/paid-parental-weeks" }
  - { s: "entity:leave_type/paid-parental",         p: "wage_rate",     o: 70, note: "percent" }
  - { s: "entity:leave_type/paid-parental",         p: "deadline",      o: "child's 1st birthday" }
  - { s: "entity:leave_type/study",                 p: "entitlement",   o: "entity:metric/study-leave-days" }
  - { s: "entity:leave_type/short-term-care",       p: "duration_fte",  o: "entity:metric/short-term-care-fte-max" }
  - { s: "entity:leave_type/short-term-care",       p: "wage_rate_legal", o: 70, note: "percent legally required" }
  - { s: "entity:leave_type/short-term-care",       p: "wage_rate_respellion", o: 100, note: "Respellion supplements to 100%" }
  - { s: "entity:leave_type/long-term-care",        p: "duration",      o: "entity:metric/long-term-care-weeks" }
  - { s: "entity:leave_type/long-term-care",        p: "wage_paid",     o: false }
  - { s: "entity:leave_type/emergency",             p: "wage_rate",     o: 100, note: "percent" }
  - { s: "entity:leave_type/feestdag",              p: "entitlement",   o: "entity:metric/interchangeable-holidays" }
  - { s: "entity:org/goed",                         p: "first_contact_after_days_sick", o: 5 }
  - { s: "entity:org/goed",                         p: "problem_analysis_after_weeks", o: 6 }
source_files:
  - { path: "docs/Anything to do with (holiday) leave/holiday-vacation-leave.md", sha: "cca8b1181f1e817e5d562b92366d4598ef944b44", lines: "1-133" }
  - { path: "docs/Anything to do with (holiday) leave/sick-leave.md",             sha: "6dffe67d3d892e45d78095f690b367d509571e1b", lines: "1-68" }
  - { path: "docs/Anything to do with (holiday) leave/parental-leave.md",         sha: "72aa88b5d8a406a6ea752c3f8aae143e8b278c2c", lines: "1-96" }
  - { path: "docs/Anything to do with (holiday) leave/special-leave.md",          sha: "dfe44a337b97e7bf0171d5802c97fd6383342765", lines: "1-131" }
related_files:
  - 01-organization-identity-and-culture.md
  - 02-daily-operations-and-workplace.md
  - 04-compensation-benefits-and-development.md
---

# Respellion: Leave and Absence Policies

> Source consolidation: this document merges the content originally distributed across the `Anything to do with (holiday) leave` section of the employee handbook into a single AI-ingestable knowledge unit.

## Glossary

| Abbreviation | Expansion |
|---|---|
| ANW | Algemene nabestaandenwet — Dutch general surviving relatives' benefits law |
| AO | Arbeidsongeschiktheid — incapacity for work |
| Arbodienst | Occupational health and safety service (Dutch) |
| Bevallingsverlof | Maternity leave (Dutch) |
| BHV | Bedrijfshulpverlening — in-house emergency response |
| FEESTDAG | Interchangeable public-holiday leave type in Exact (Dutch: "holiday") |
| GOED | Health and Safety Provider used by Respellion |
| Geboorteverlof | Partner / paternity birth leave (Dutch) |
| Mantelzorg | Informal care (Dutch) |
| TfT | Tijd-voor-tijd (Time-for-time) |
| UWV | Uitvoeringsinstituut Werknemersverzekeringen — Dutch Employee Insurance Agency |
| Verlof | Leave (Dutch) |
| WAZO | Wet Arbeid en Zorg — Work and Care Act (Dutch) |
| WVP | Wet Verbetering Poortwachter — "Gatekeeper Improvement Act" (Dutch) |
| Zwangerschapsverlof | Pregnancy leave (Dutch) |
| Zwangerschapsverklaring | Pregnancy declaration letter (Dutch) |

<!-- source: docs/Anything to do with (holiday) leave/holiday-vacation-leave.md#L1-L133 sha:cca8b11 -->
## 1. Holiday and Vacation Leave

### 1.1 Leave procedure

When you take leave, you'll, of course, have a critical look at your calendar and your colleagues and make sure that your colleagues know that you are not there before you take leave. The administration is done in "Shifts" within Microsoft Teams.

Make a new Request for Time-Off in Microsoft Shifts with the right category. This also includes Sick Leave.

Your request will be approved by the People Officer after which the leave will be visible in Shifts to the whole team.

Create an event in your own calendar for your holiday to ensure your agenda is blocked.

If you are not sure whether your leave falls under holiday hours but, for example, under care or a sudden absence, please contact the People Officer role, so together we can have a look at the possibilities. Also take a look on the paragraph 📆 Sick Leave and 📆Special Leave, for more info.

### 1.2 Leave administration in Exact

**1. Basic Principles**

- **Time sheets are for Productive Hours:** In the time sheet administration, you only register productive hours. These include hours for clients, internal projects, work meetings, or business development. Absences such as leave should not be registered here.
- **Leave Administration for Absences:** All forms of absence, such as regular leave, special leave, and time-for-time, are registered via the leave registration module in Exact.
- **Time-for-Time (TfT):** If you work more hours than your contract stipulates in a month, these extra hours will be added to your TfT balance at the beginning of the following month.

**2. How to Register Regular Leave**

1. In Exact Online, navigate to the **Leave Registration** module.
2. Click on **"Create leave registration"**.
3. Select your own name.
4. Under **Leave Type**, choose **"Verlof" (Leave)**.
5. In the **Description field**, note the dates and the number of hours you wish to take off.
6. Upon approval, this will be automatically deducted from your leave balance (statutory hours are used first, followed by non-statutory hours).

**3. How to Register Time-for-Time (TfT)**

**1. Accrual:** At the beginning of each month, the overtime hours from the previous month are manually added to your TfT balance. You will see this as a separate balance in your leave administration.

**2. Taking Leave:**
- Go to **Leave Registration** in Exact.
- Click on **"Create leave registration"**.
- Select your own name.
- Under **Leave Type**, choose **"Tijd-voor-tijd" (Time-for-time)**.
- Enter the number of hours you wish to take.
- **Please note:** Ensure you do not create a negative TfT balance.

### 1.3 Vacation leave

If you work full-time, you are entitled to 25 vacation days. Of these, 20 are statutory, and 5 are non-statutory.

If you work part-time, this will be calculated based on the amount of time you work. The same applies when you start or stop employment mid-year.

We think it's important to chill for a considerable amount of time during the year. And when we say this, we really mean relax and not think about work. That's why you must take two consecutive working weeks of vacation a year.

### 1.4 How to take (annual) leave

You need to apply for leave in advance. This is done in "Shifts" within Microsoft Teams. Coordinate within your circle who is on holiday and when, and make sure that the important things or certain tasks are transferred to your colleagues during the time when you're on vacation.

When you become ill unexpectedly during your vacation, you will keep your vacation days. Read more in the paragraph about illness.

### 1.5 Vacation days that have not been used

If the situation occurs that by the end of the year you haven't used up your full vacation hours, then you can bring 80 hours of leave (working on a full-time base) to the new year. The statutory days will expire 6 months after the calendar year in which you've accrued them. For example, the vacation days that you received in 2024 but did not use will expire on July 1st 2025.

An exception can be made if you were chronically ill.

Non-statutory supplementary days expire after 5 years.

We find it important that you get days off, therefore it is not intended to save up leave time. That is why we don't pay in exchange for days off.

An upper and lower limit of the leave balance is set on January 1st of each year. On January 1st of each year, a negative balance of one week of contracting hours is permitted. On January 1st of each year, the number of extra non-statutory vacation hours may not exceed twice the amount of contracting hours per week. When the minimum or maximum is reached, taking or saving hours of leave is only permitted again after leave hours have been added to or taken from the balance.

In the case of leave exceeding the upper limit at the end of the calendar year, agreements will be made to reduce the credit as soon as possible.

### 1.6 Holidays

On the following days, you can write a cross in your calendar. You get a day off on:

- New Year's Day (January 1st)
- Easter Monday
- King's day (April 27)
- Liberation Day in the anniversary year (May 5th 2025/2030)
- Ascension Day
- Whit Monday
- Both Christmas Days (December 25th and 26)

You may also leave a bit earlier (one hour earlier) on:

- Good Friday
- 5th of May on the non-lustrum years
- the day before Christmas
- New Year's Eve

This is a small compensation for those who are working these special days. So taking the day off will cost you the normal 8 hours. There is no extra compensation for public holiday leave that falls on your standard schedule-free day in case of part time employment.

The days of public holidays are by default greyed out in Exact. However, you do need to register holiday leave on this day and if, in any case, you need to work on these days you can register these hours on your project.

### 1.7 Interchangeable Holiday policy

We want to be an inclusive organization, so we have the Interchangeable Holiday Policy. With this policy, you may exchange 4 national Dutch holidays per year for any other day of your choice. By doing this, we hope to offer a more inclusive arrangement for colleagues who, for example, but not limited to, prefer to celebrate Eid al-Fitr (also referred to in the Netherlands as Suikerfeest), Thanksgiving, Yom Kippur, your birthday or Christmas Eve.

If you want to take another day off instead of the regular public holidays, you request a day of leave with "verlofsoort" FEESTDAG.

---

<!-- source: docs/Anything to do with (holiday) leave/sick-leave.md#L1-L68 sha:6dffe67 -->
## 2. Sick Leave

Respellion wishes to provide a good physical and psychological working environment and strives towards making the workplace an attractive place for the individual as well as preventing absence due to illness, by offering an exciting daily worklife with unique development opportunities. We believe that open and honest communication will help to reduce absenteeism, support and retain long-term employees even when dealing with difficult and sensitive issues.

The sickness and absence policy is made in respect of the employees on leave and the overall operation of the company, in order to accommodate everyone. We all have an obligation to be aware of each other's mental and physical well- being, so it is important that we help each other. Respellion has relevant and competent experience in this area and will support the employee as much as possible, while the individual employee is respectfully obligated to keep Respellion informed.

According to the (in Dutch) Wet Verbetering Poortwachter (WVP), the employee and employer are jointly responsible for resuming work as quickly as possible in the event of incapacity for work due to illness.

We will briefly explain a few points below. We have a separate Absenteeism Protocol that describes this more extensively.

### 2.1 Reporting sick

If you want to call in sick, you can contact the people officer role by phone in the morning between 8:30 and 9:00. During the phone call, this colleague will ask you when you think you will be better and discuss what you are working on and what may need to be transferred. The people office role will communicate your absence in Microsoft Teams.

If you become ill during the working day and want to go home, report this personally to the people officer role. When you have recovered, we kindly ask you to call the role people officer.

### 2.2 During your sickness

When you are sick, make sure you are available on your phone so that we or the external health service (Arbodienst) can reach you. We will keep in touch to hear how you're doing. When your nursing address changes, you must also inform us.

The "Wet Verbetering Poortwachter" sets out the efforts both you and Respellion need to make to speed up your recovery. In the Absenteeism Protocol you can find more information about this. Make sure you read this when you are sick.

### 2.3 Company doctor

If you are sick for approx. five days, the Medical Case manager of the Health and Safety Provider named GOED will probably contact you. During this conversation, questions will be asked regarding your health issues. Expect questions about prescribed medications, physical/ mental struggles or issues related to work or private life that could affect your health. Try to answer the questions in the best possible manner. That way, the medical case manager can help/ guide you accordingly during this time of illness. This call will take place unannounced.

When you have been ill for (almost) 6 weeks, a next appointment will be scheduled. This appointment will be held so that a Problem Analysis can be made. A written report will follow, ask the contact person at GOED for log-in details so you can view the Problem Analysis.

Do you dread it? Don't worry, all these steps are here to help/support you! Feel free to contact the People Officer when you are nervous about this. Together you can prepare for this conversation, so any doubts or insecurities can be addressed before this scheduled appointment with the Medical Case manager of the Health and Safety Provider named GOED.

▶️ Last but not least: all medical conversations with GOED are confidential, the employer will not receive any details.

### 2.4 Obligation to continue payment of wages

If you cannot work due to illness, we will continue the payment of the salary for the first year in full. In the second year wages of 70% are paid.

### 2.5 Sick during holidays

If you become ill during your holiday, you must inform us as soon as possible, i.e. by telephone, stating your holiday address. After your return, you must be able to submit a 'medical certificate' (drawn up by a doctor during the illness) to the occupational health and safety service. This medical certificate states the duration, nature and treatment of the incapacity for work. Based on this declaration, the occupational health and safety service will advise Respellion on the return of holidays.

### 2.6 On holiday during illness

If you want to take time off during the period of illness, to go on holiday, you do so in consultation. Sometimes you will need a 'statement of no objection' from the occupational health and safety service. With this statement, you can submit a request to be allowed to go on holiday. We will decide whether to grant the holiday. Your holiday should never be an obstacle to your recovery.

### 2.7 Taking leave during reintegration

When taking leave, colleagues who can partly perform their own work will have to deduct the days of leave for the entire working day/week from their leave balance. This is because you have also accrued the balance of leave over the entire working hours.

For example: you have a 36-hour contract, and you are 50% incapacitated for work. So you are currently working 18 hours a week, temporarily. Do you want free time during this reintegration? Then you must apply for 36 holiday hours.

---

<!-- source: docs/Anything to do with (holiday) leave/parental-leave.md#L1-L96 sha:72aa88b -->
## 3. Parental Leave

This policy document outlines the parental leave entitlements for Respellion. The policy is aligned with the current Dutch regulations as stipulated in the Work and Care Act (Wet Arbeid en Zorg).

### 3.1 Maternity Leave

#### 3.1.1 Entitlement

Female employees are entitled to 16 weeks of fully paid maternity leave. For multiple births (e.g., twins or triplets), this is extended to 20 weeks.

#### 3.1.2 Breakdown of Maternity Leave

- Pregnancy Leave (Zwangerschapsverlof): 4-6 weeks before the expected due date.
- Maternity Leave (Bevallingsverlof): 10-12 weeks after childbirth.

#### 3.1.3 Important Points

- It is mandatory to take at least 4 weeks of leave before the expected due date.
- If an employee chooses to take less than 6 weeks before the due date, the remaining days will be added to the maternity leave period.
- If the baby is born later than the due date, the period between the due date and the actual birth date is added to the total leave period.
- If the employee becomes ill due to pregnancy before maternity leave is due to start, maternity leave may automatically commence 6 weeks before the estimated delivery date.
- If the baby is hospitalized immediately after birth, maternity leave starts the day after the mother and baby leave the hospital.
- During maternity leave, employees receive 100% of their salary.
- Employees must inform their employer about their intention to take maternity leave at least 3 weeks in advance.
- Holiday hours continue to accrue during maternity leave.

### 3.2 Partner / Paternity Leave

#### 3.2.1 Entitlement

Partners (including same-sex partners) of women who have given birth are entitled to:

- 1 week (5 working days) of fully paid birth leave (geboorteverlof)
- 5 weeks of additional birth leave (aanvullend geboorteverlof) at 70% of their salary

#### 3.2.2 Important Points

- The initial 1 week of leave must be taken within the first 4 weeks after the birth.
- The additional 5 weeks must be taken within the first 6 months after the birth.
- The additional leave can be taken all at once or spread out over the 6-month period.
- To take the additional leave, employees must submit a request via the regular leave request procedure at least 4 weeks in advance.
- Employers can only adjust the timing if the leave would cause serious organizational problems, and must finalize any changes no later than 2 weeks before the scheduled leave.
- During the additional leave, the UWV pays 70% of the employee's salary (up to the maximum daily wage).
- Holiday hours continue to accrue during partner leave.

### 3.3 Parental Leave

#### 3.3.1 General Information

- Parental leave is available for all employees who are parents or legal guardians of children under the age of 8.
- Each parent is entitled to 26 times their weekly working hours of parental leave per child.
- For example, an employee working 40 hours per week is entitled to 1,040 hours (26 × 40) of parental leave per child.
- Parental leave applies to each child separately. For multiple births or adoptions, the entitlement applies to each child.
- Parents with a "family relationship" with the child (biological parents, adoptive parents, foster parents, and step-parents who live with and take care of the child) are eligible.

#### 3.3.2 Unpaid Parental Leave

- Unpaid parental leave can be taken until the child reaches the age of 8 years.
- The leave can be taken in one block or spread out over time.
- No vacation hours are accumulated over the unpaid parental leave.
- If an employee falls ill during parental leave, the leave continues as normal.
- Employees should discuss how they wish to implement the leave with the people officer at least 2 months before the desired start date.

#### 3.3.3 Paid Parental Leave

- Of the total 26 weeks of parental leave, 9 weeks can be taken as paid parental leave.
- The paid leave must be used before the child reaches the age of 1 year.
- During paid parental leave, the employee receives a benefit of 70% of their daily wage.
- This benefit is applied for by the employer to the UWV and the salary is adjusted accordingly.
- The benefit can only be applied for entire work weeks.
- Vacation hours are accumulated over the paid parental leave.
- All other conditions that apply to unpaid parental leave also apply to paid parental leave.

### 3.4 Application Process

#### 3.4.1 For Maternity Leave

1. The employee must inform the people officer of their pregnancy and intended maternity leave at least 3 weeks before the leave is to start (preferably earlier).
2. The employee must provide a pregnancy declaration letter (zwangerschapsverklaring) from their midwife or gynecologist.
3. The employer will complete a WAZO form (maternity and childbirth benefit form) and send it to the UWV.

#### 3.4.2 For Partner / Paternity Leave

1. For the initial week of leave, the employee should notify their employer as soon as possible after the birth.
2. For the additional 5 weeks, the employee must submit a request via the regular leave request procedure at least 4 weeks in advance## .

#### 3.4.3 For Parental Leave

1. The employee must submit a written request via the regular leave request procedure at least 2 months before the desired start date.
2. The request should specify how they wish to take the leave (all at once or spread out).
3. After consultation, the employer will confirm the leave arrangements in writing.

#### 3.4.4 For Adoption or Foster Care Leave

1. The employee must notify their employer at least 3 weeks before they want the leave to start.
2. The employee should indicate whether they want to take their leave all at once or spread it out.

---

<!-- source: docs/Anything to do with (holiday) leave/special-leave.md#L1-L131 sha:dfe44a3 -->
## 4. Special Leave

### 4.1 Vacation leave

Please see 🏝️[Holiday and vacation leave](https://employeehandbook.respellion.nl/Anything%20to%20do%20with%20%28holiday%29%20leave/holiday-vacation-leave/)

### 4.2 Study leave

For every year, you are entitled to 5 days of study leave based on a 40-hour work week, which will be calculated pro rata if you work part-time. These will expire on 31 December. You can use the study leave if your selected training takes place during working hours. You can apply for leave by using the request for leave procedure.

### 4.3 Unpaid leave

Employees with a permanent contract have the option of applying for unpaid leave for up to 12 months for educational purposes, travel or other special activities requiring a longer leave of absence from work. This can also be used for short term leave for instance extra vacation. The following rules apply:

- Vacation days must be used first in order to request unpaid leave.
- Applications for leave are submitted to the People Officer role.
- It is necessary to provide as much notice as possible of (long term) sabbatical leave; at least 3 months before the preferred start date.
- No salary will be paid by during the agreed period and benefit arrangements can be suspended.
- In the days that you take unpaid leave, you do not build up holiday pay, no holiday hours, no unemployment rights and no pension. You can read more about this on the Rijksoverheid webpage.
- If the employee falls ill during the leave, he / she is not entitled to continued payment of salary during the period of unpaid leave.
- Up to one month of the unpaid leave, employer will keep paying for pension scheme. After one month pension scheme will not be paid, until the employee resumes his daily work.
- In case of a longer period of unpaid leave, you will not receive a travel allowance (nor an internet allowance and other related allowances).
- Taking unpaid leave could affect your annual salary raise
- Suppose you choose to take unpaid leave for a duration of two months or more throughout the entire calendar year in addition to your regular holiday leave and purchased holiday leave. In that case, the standard salary raise will not be implemented. As a result, you will not qualify for an annual salary raise if your leave extends for 3,5 months or more, encompassing both paid and unpaid leave periods.

### 4.4 Special leave for activities and (family) situations

There may be special situations where you are not able to work. The following are the most common situations. In these cases, you are entitled to special leave with full pay. Common sense applies here. If, for example, you are invited to a wedding reception only at the end of the day, you do need to work in the morning. You can apply for leave by using the regular request for leave procedure.

| Situation                                                                                                                                                      | Maximum special leave                                           |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| Deposition for marriage                                                                                                                                        | 1 day                                                           |
| Marriage or registered partnership of yourself                                                                                                                 | 2 days                                                          |
| Marriage or registered partnership of a child, brother, sister, parent, parent-in-law, brother-in-law or sister-in-law, provided that the ceremony is attended | 1 day                                                           |
| Moving house                                                                                                                                                   | 1 day per calendar year                                         |
| Paternity leave                                                                                                                                                | 1 workweek and max 5 weeks additional                           |
| Spouse/partner, relatives by blood or marriage of the 1st degree passing away                                                                                  | From the day of death until the day of the funeral or cremation |
| Relatives by blood or marriage of the 2nd degree passing away                                                                                                  | 2 days the day of death and the day of the funeral or cremation |
| Relatives by blood or marriage of the 3rd and 4th degree passing away                                                                                          | The time to attend the funeral or cremation                     |
| Necessary doctor's visit which cannot take place outside of working hours                                                                                      | Max 8 hours on a yearly basis, see explanation below            |
| 12,5 / 25-year relationship with your partner                                                                                                                  | 1 day                                                           |

### 4.5 Doctor's visit

A doctor's visit means a visit to the doctor, the dentist, a specialist or a therapist to which you are referred. You plan it in your own time, if that is not possible then consult with your circle which times are convenient (e.g. beginning or end of the working day). We continue payment of the salary for the time that is needed for the doctor's visit, within the working day, to a maximum of two hours per visit. For seeing a specialist there is a maximum of four hours per visit. You will work the remaining hours before or after the doctor's visit. The maximum number of hours to be reimbursed can not exceed 8 on an annual basis. In special cases, there can be a deviation of this, in consultation with the employer.

### 4.6 'Other' Special Leave Situations — non-family

Other personal situations: like loved ones passing away or a marriage or anniversary of non-family members.

Of course, happy or unpleasant things can also happen to non-family members. Therefore, we want to provide leave for these situations. The assessment of whether you want to make use of these days is up to you, but please consult the People Officer role upfront. Some examples: marriage or funeral of a person that is important to you.

### 4.7 Maternity / Paternity / Parental Leave

We have a separate page for 🐥[Maternity / Paternity / Parental Leave](https://employeehandbook.respellion.nl/Anything%20to%20do%20with%20%28holiday%29%20leave/parental-leave/).

### 4.8 Emergency leave, short-term and long-term care related leave

Working flexibly is very normal in our organization. You get the opportunity to organize your own working hours according to your own preferences. Working from home, even in the evenings, is no problem. So if you can not work during the daytime because of some reason, it is fine with us if you finish it at another time. We give you a lot of freedom and responsibility and trust that you know how to use it well.

If there are urgent private circumstances that are of a very serious nature, you may be eligible for emergency leave, short-term medical care leave, or long-term care leave. Our starting point for this is the legal framework of the Work and Care Act (Wet Arbeid en Zorg). We would like to look at the possibilities with you.

You report the situation of force majeure immediately to the role People Officer. If this is not possible, report it as soon as possible. We may require that you demonstrate to us that you really haven't been able to work as a result of one of the given reasons. For example, by submitting a medical certificate. In addition, we keep track of these hours.

| Emergency                                                                                     | Short term                                                                                                 | Long term                                                            |
| --------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------- |
| Keywords: unforeseen, serious, short-term (such as arranging care).                           | Keywords: you're the only one who can care for your very sick (life-threatening) child, spouse, or parent. | Keywords: for necessary care for others, in case of serious illness. |
| f.e. picking a sick child up from daycare. Waiting for the plumber to fix a burst water pipe. | f.e. helping partner at home, with medical tasks when he/she just had surgery                              | f.e. caring for a terminally ill partner                             |
| Paid leave, 100%                                                                              | Paid leave, 70%, fully supplemented                                                                        | Unpaid leave                                                         |

### 4.9 Emergency leave

Emergency leave is applicable if there has been an unforeseen emergency with the employee, that can not be delayed. One example is a sudden hospitalization of an immediate family member or your partner giving birth. The length of the leave is dependent on the situation, but presumably cannot be longer than one day. Emergency leave is intended for initial care and arranging a structural solution. We expect you to go back to work as soon as the emergency has been resolved. It is possible that the emergency leave becomes short-term care leave. We are obligated as an employer to pay the full salary of the employee during the emergency leave.

__Keywords: unforeseen, serious, short-term (such as arranging care)__

### 4.10 Short-term medical care leave

You may submit a request for short-term care leave if it is necessary to care for a sick partner or resident children. Short-term care is applicable when you are the only person who has to take care of an immediate family member (child, spouse or parent).

Short-term care takes up to two times the hours worked in a week. So 80 hours per year for a full-time workweek. You can also take days alternately. By law we are required to pay 70% of the salary, we choose to pay your salary during short-term care leave fully.

If the period of short-term care is not enough then you can also have unpaid long-term care in case of a very serious illness.

The employer may ask to give a reason for the leave once you return. Care leave may be refused by the employer if there are valid reasons to do so. For example, if the company will get in trouble because of the absence of the employee.

For the application of this Act (WAZO) the term "life-threatening illness" shall mean a state of health that is so serious that according to objective medical standards the person's life is in serious danger in the short term.

For the purpose of this Act the term "needy" (in need of assistance) is understood to mean: the condition of a person as a result of which he requires assistance for self-reliance, participation, protected living or shelter that is not provided within the framework of a professional providing assistance and that exceeds the usual assistance.

Taking this leave will affect the amount of your untaxed allowances such as the home working allowance and possibly internet or telephone allowance.

__Keywords: you're the only one who can care for your very sick (life-threatening) child, spouse or parent__

### 4.11 Long-term care leave

Long-term care is possible in case of a seriously ill spouse, child or parent of the employee. From July 1, 2015 you can also take long-term care leave when it comes to necessary care (helplessness or illness) for grandparents, grandchildren, brothers/sisters, other housemates and people with whom you have a social relationship and are dependent on the help of the employee. The payment of the salary won't be continued during the period of the long-term care leave. The employer may only refuse permission in case of substantial business interests. You can take 6 weeks of long-term care leave a year, distributed over 18 weeks.

For the application of this Act (WAZO) the term "life-threatening illness" shall mean a state of health that is so serious that according to objective medical standards the person's life is in serious danger in the short term.

For the purpose of this Act the term "needy" (in need of assistance) is understood to mean: the condition of a person as a result of which he requires assistance for self-reliance, participation, protected living or shelter that is not provided within the framework of a professional providing assistance and that exceeds the usual assistance.

Taking this leave will affect the amount of your untaxed allowances such as the home working allowance and possibly internet or telephone allowance.

__Keywords: unpaid, for necessary care for others, in case of serious illness__

### 4.12 Informal care ('mantelzorg')

The official definition used by the government: Caregivers provide unpaid care for a chronically ill, handicapped, or helpless partner, parent, child, or another family member, friend or acquaintance for more than 8 hours per week and/or more than 3 months. A caregiver didn't choose to provide care, it happens to someone because that person has an emotional attachment to the person who needs care.

The practice has shown that care and work can be combined, as long as it is managed correctly. Both by the organization and by you. In this way, overload can be prevented, and caregivers keep both their work and their family responsibilities well-balanced and properly implemented. Research shows that giving visibility to informal care and discussing it can provide very good solutions. Are you a caregiver? Then talk about it with your colleagues and the Request for Leave role, so together we can look at the possible support options there may be in addition to leave. That's how we will find workable solutions so that informal care and work can be better combined.

Taking this leave will affect the amount of your untaxed allowances such as the home working allowance and possibly internet or telephone allowance.
