---
id: kb-02-daily-operations-and-workplace
title: "Respellion: Daily Operations and Workplace Practices"
description: "Consolidated reference for day-to-day operational policies at Respellion: office presence, office etiquette, overtime and flexible hours, time-for-time administration, time registration in Exact, travel time policy, and printing (PaperCut Hive)."
category: operations
language: en
audience: [employee]
version: 1.1.0
last_updated: "2026-05-18"
last_source_commit: fb9a84a
topics:
  - office-presence
  - hybrid-work
  - office-etiquette
  - overtime
  - flexible-hours
  - time-for-time
  - tft
  - time-registration
  - exact-online
  - travel-time
  - printer
  - papercut-hive
  - hour-types
key_entities:
  systems_and_tools:
    - Outlook Calendar
    - Exact Online
    - Microsoft Shifts
    - Microsoft Teams
    - NS business card
    - PaperCut Hive
    - SharePoint
  policies_and_concepts:
    - "Time-for-Time (TfT)"
    - "Time-for-Time at 100%"
    - "Weekend compensation: 175%"
    - "Public holiday compensation: 300%"
    - "Travel time threshold: 1.5 hours one-way"
    - "Savings maximum: 24 hours above the normal non-statutory balance"
    - "Project codes: TM, FPP, INTBD001"
  roles:
    - People Officer
    - THT team
  external_references:
    - "Exact Leave Registration"
    - "Outlook Manual (SharePoint)"
entities:
  - { id: "entity:org/respellion",              type: organization, label: "Respellion" }
  - { id: "entity:tool/outlook-calendar",       type: tool, label: "Outlook Calendar" }
  - { id: "entity:tool/exact-online",           type: tool, label: "Exact Online" }
  - { id: "entity:tool/microsoft-shifts",       type: tool, label: "Microsoft Shifts" }
  - { id: "entity:tool/microsoft-teams",        type: tool, label: "Microsoft Teams" }
  - { id: "entity:tool/sharepoint",             type: tool, label: "SharePoint" }
  - { id: "entity:tool/papercut-hive",          type: tool, label: "PaperCut Hive" }
  - { id: "entity:tool/ns-business-card",       type: tool, label: "NS business card" }
  - { id: "entity:role/people-officer",         type: role, label: "People Officer" }
  - { id: "entity:role/tht-team",               type: role, label: "THT team" }
  - { id: "entity:concept/time-for-time",       type: concept, label: "Time-for-Time", aliases: ["TfT", "Tijd-voor-tijd"], lang: en }
  - { id: "entity:concept/overtime",            type: concept, label: "Overtime" }
  - { id: "entity:value/self-discipline",       type: concept, label: "Self-discipline" }
  - { id: "entity:project/tm",                  type: concept, label: "Time and Material project", aliases: ["TM"] }
  - { id: "entity:project/fpp",                 type: concept, label: "Fixed Price Project", aliases: ["FPP"] }
  - { id: "entity:project/intbd001",            type: concept, label: "Project INTBD001 - Business Development", aliases: ["INTBD001"] }
  - { id: "entity:leave_type/verlof",           type: leave_type, label: "Verlof (Leave)", lang: nl }
  - { id: "entity:leave_type/tijd-voor-tijd",   type: leave_type, label: "Tijd-voor-tijd (Time-for-time)", lang: nl }
  - { id: "entity:metric/tft-savings-maximum",  type: monetary_constant, label: "Time-for-Time savings maximum", value: 24, unit: "hours" }
  - { id: "entity:metric/weekday-overtime-rate", type: metric, label: "Weekday overtime compensation rate", value: 100, unit: "percent" }
  - { id: "entity:metric/weekend-overtime-rate", type: metric, label: "Saturday/Sunday overtime compensation rate", value: 175, unit: "percent" }
  - { id: "entity:metric/holiday-overtime-rate", type: metric, label: "Public holiday overtime compensation rate", value: 300, unit: "percent" }
  - { id: "entity:metric/travel-time-threshold", type: metric, label: "Travel time threshold (one-way, not compensated)", value: 1.5, unit: "hours" }
  - { id: "entity:metric/travel-time-ratio",    type: metric, label: "Travel time compensation ratio beyond threshold", value: "1:1" }
relations:
  - { s: "entity:org/respellion", p: "uses_tool", o: "entity:tool/outlook-calendar", note: "for planned presence (Remote / Office)" }
  - { s: "entity:org/respellion", p: "uses_tool", o: "entity:tool/exact-online", note: "financial administration and time registration" }
  - { s: "entity:org/respellion", p: "uses_tool", o: "entity:tool/papercut-hive", note: "office printing" }
  - { s: "entity:concept/time-for-time", p: "compensates_at", o: "entity:metric/weekday-overtime-rate" }
  - { s: "entity:concept/overtime", p: "compensates_at", o: "entity:metric/weekend-overtime-rate", note: "Saturdays and Sundays" }
  - { s: "entity:concept/overtime", p: "compensates_at", o: "entity:metric/holiday-overtime-rate", note: "public holidays" }
  - { s: "entity:concept/time-for-time", p: "savings_capped_at", o: "entity:metric/tft-savings-maximum" }
  - { s: "entity:concept/time-for-time", p: "registered_in", o: "entity:tool/exact-online" }
  - { s: "entity:concept/time-for-time", p: "registered_as", o: "entity:leave_type/tijd-voor-tijd" }
  - { s: "entity:org/respellion", p: "travel_threshold", o: "entity:metric/travel-time-threshold" }
  - { s: "entity:org/respellion", p: "travel_compensation_ratio", o: "entity:metric/travel-time-ratio" }
  - { s: "entity:role/people-officer", p: "registers_sick_leave_in", o: "entity:tool/exact-online" }
  - { s: "entity:role/tht-team", p: "supports", o: "entity:tool/papercut-hive" }
source_files:
  - { path: "docs/Day to day/office-presence.md",         sha: "2ac2ae56d30f8e89eef644b8d5173ca887cabaaf", lines: "1-6" }
  - { path: "docs/Day to day/office-etiquette.md",        sha: "f6b7982d02c09346e637e8bca45c9dc4d3d8dd52", lines: "1-12" }
  - { path: "docs/Day to day/overtime-flexible-hours.md", sha: "243253e70b449edfa6c8b3fb04b0c19acd3b84f9", lines: "1-43" }
  - { path: "docs/Day to day/time-registration.md",       sha: "4bd1b0f755df2f36226c875844a03638cd1c5828", lines: "1-27" }
  - { path: "docs/Day to day/travel-time-policy.md",      sha: "70d243ba24a21131922a044922da49abcf42e2e8", lines: "1-11" }
  - { path: "docs/Day to day/printer.md",                 sha: "97d0b775442baa99bbf9cf25fbb04202466269c2", lines: "1-14" }
related_files:
  - 01-organization-identity-and-culture.md
  - 03-leave-and-absence.md
  - 04-compensation-benefits-and-development.md
---

# Respellion: Daily Operations and Workplace Practices

> Source consolidation: this document merges the content originally distributed across the `Day to day` section of the employee handbook into a single AI-ingestable knowledge unit.

## Glossary

| Abbreviation | Expansion |
|---|---|
| FPP | Fixed Price Project |
| TfT | Tijd-voor-tijd (Time-for-time) |
| THT | The Hague Tech |
| TM | Time and Material project |
| NS | Nederlandse Spoorwegen (Dutch railways) |
| INTBD001 | Internal Business Development project code in Exact |
| Uursoort | Hour type / category in Exact time registration (Dutch) |

<!-- source: docs/Day to day/office-presence.md#L1-L6 sha:2ac2ae5 -->
## 1. Office Presence

To keep track of who is in the office and when, you can set your planned presence in Outlook Calendar. For each workday, indicate whether you expect to be working from home (Remote) or at the office (Office).

Of course, not every week is the same. In that case, select your average presence and then adjust this in the weekly overview for the days that deviate from the schedule.

[See further instructions in the manual](https://respellion.sharepoint.com/sites/Company/Shared%20Documents/Forms/AllItems.aspx?id=%2Fsites%2FCompany%2FShared%20Documents%2FHandleiding%20%2D%20Locatie%20instellen%20in%20Outlook%2Epdf&parent=%2Fsites%2FCompany%2FShared%20Documents).

---

<!-- source: docs/Day to day/office-etiquette.md#L1-L12 sha:f6b7982 -->
## 2. Office Etiquette

At Respellion, we strive for a productive and respectful work environment for everyone, including during remote meetings held from the office. To minimize disruptions and ensure optimal concentration, the following guidelines apply:

- **Larger meetings and demonstrations:** For meetings with multiple participants or for demonstrations, it is essential to reserve a separate meeting room. This ensures that others in the open-plan office are not disturbed and that meeting participants can concentrate optimally.

- **Individual calls and short discussions:** Brief, individual calls or quick discussions via a remote connection are acceptable in the open office space. However, always be mindful of your volume and try to cause as little inconvenience as possible to your colleagues. Keep the duration of such calls in the open space limited.

These guidelines contribute to our collective well-being and efficient way of working, in line with our core values such as trust and self-discipline, which are also reflected in our ability to be considerate of one another.

---

<!-- source: docs/Day to day/overtime-flexible-hours.md#L1-L43 sha:243253e -->
## 3. Overtime and Flexible Hours

At Respellion, we strive for a sustainable and healthy work-life balance. This aligns directly with our core value of Self-Discipline. We trust that as a professional, you take personal responsibility for maintaining healthy working hours. These guidelines provide a framework to facilitate flexibility, protect you, and simultaneously offer the autonomy that fits our culture. In exceptional cases, there is always the opportunity to discuss possibilities.

### 3.1 Framework for flexibility and saving hours (Employee's Choice)

We understand that you may need flexibility. Therefore, it is possible to manage your contract hours flexibly within a month or so to work extra hours to save for time off at a later moment. There is no obligation to use these saved hours within a specific period.

- **Time-for-time as the basis:** Hours you work beyond the daily norm are automatically processed as saved leave hours. These hours are compensated on a 1-for-1 basis (100%) on weekdays.
- **Savings Maximum:** To maintain balance, there is a maximum of 24 hours above the normal non-statutory balance.
- **Personal Responsibility:** It is your responsibility to monitor your saved hours balance and to take your time off promptly to avoid exceeding the 24-hour limit. This is a direct example of the self-discipline we value highly at Respellion.

#### Administration

**Time-for-Time (TfT):** If you work more hours than your contract stipulates in a month, these extra hours will be added to your TfT balance at the beginning of the following month.

**1. Accrual:**
At the beginning of each month, the overtime hours from the previous month are manually added to your TfT balance. You can see this as a separate balance in your leave administration.

**2. Taking Leave:**
- Go to **Leave Registration** in Exact.
- Click on **"Create leave registration"**.
- Select your own name.
- Under **Leave Type**, choose **"Tijd-voor-tijd" (Time-for-time)**.
- Enter the number of hours you wish to take.
- **Please note:** Ensure you do not create a negative TfT balance.

### 3.2 Overtime by Assignment (Client Necessity)

While our policy is aimed at preventing overtime, it may occur that a client requests extra effort. In such cases, the following framework applies:

- **Consultation is crucial:** Overtime at a client's request always takes place in consultation and approval with the responsible role. We will take your personal situation into account as much as possible.
- **Compensation:** Overtime on weekdays is standardly compensated with time-for-time (100%). For necessary work on Saturdays, Sundays, and public holidays, significantly higher compensation rates apply: 175% for weekend days and 300% for public holidays. These hours are also primarily compensated in time.

### 3.3 Payout of Saved Hours

We offer the option to have saved hours paid out. It is your own responsibility to indicate in a timely manner if you wish to have saved hours paid out. This aligns with the entrepreneurial attitude we encourage in all our colleagues.

---

<!-- source: docs/Day to day/time-registration.md#L1-L27 sha:4bd1b0f -->
## 4. Exact Time Registration

We use Exact online as financial administration and for time registration in projects, internal activities and absence.

In the following instruction you can find the steps that you need to do, to register your hours on the various types.

You need to register all contract hours, so if you work 36 hours, you register only 36 hours.

- Mind that you register your hours according to the appropriate project type, either Time and Material (TM) or Fixed Price Projects (FPP).
- With regard to registering your absence: Please **do not** register hours of absence in your time registration for your project(s). You can simply leave these empty in your daily or weekly registration.
- Time spent on internal activities needs to be specified on the correct "Uursoort" in project **INTBD001 - Business Development**
- Time spent on our werk en rol overleggen have a specific "uursoort".

### 4.1 Sickness registration

When you are ill, you do not need to register any hours in Exact yourself.
Do report your illness to the people officer role, according to the procedure in our absence protocol. The people officer will then ensure your sick leave is registered correctly in Exact.

---

<!-- source: docs/Day to day/travel-time-policy.md#L1-L11 sha:70d243b -->
## 5. Travel Time Policy

At Respellion, we recognize that business travel is sometimes necessary to serve our clients effectively. This policy outlines how travel time is compensated, ensuring a fair balance between business needs and personal time. The following guidelines have been established to provide clarity on travel time compensation for all employees.

- Employees may claim travel time that exceeds 1.5 hours (one-way).
- For any single journey, the first 1.5 hours of travel time (one-way) is considered personal time and will not be compensated.
- Any travel time beyond 1.5 hours per single journey can be registered and will be compensated at a 1:1 ratio.
- This policy applies to occasional travel requirements. For structural travel patterns that consistently exceed this threshold, individual arrangements may be discussed.
- Employees should register travel time using the appropriate hour type in the time registration system.

---

<!-- source: docs/Day to day/printer.md#L1-L14 sha:97d0b77 -->
## 6. Printer — PaperCut Hive

We can print documents with the PaperCut Hive service which requires to create an account. This system will handle all your printing. PaperCut will guide you through the setup process, but here's a quick overview:

### 6.1 From your computer

Once you've created your account, you'll access the User Portal. Under the Home tab, you'll see your Access Code. When you print something from your computer, you can use this code directly on the printer to view and release your print jobs.

Before printing, make sure you've downloaded the printer onto your computer. You can find the download link under "Set up my devices" in the portal. Once installed, the printer will appear in your list of available devices, and you can send your print jobs there.

### 6.2 From your phone

You can also print from your mobile device! Download the app (the link is also under "Set up my devices") and connect it to your account. You'll be able to print from both your computer and phone, view your print queue in the app, and adjust things like color, double-sided printing, and number of copies before hitting "Print release."

For more detailed instructions, check the "How to print" section in the User Portal.

If something doesn't work or you get stuck, don't worry, just reach out to someone from the THT team and they'll help you out.
