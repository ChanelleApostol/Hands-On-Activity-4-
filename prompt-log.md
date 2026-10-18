## Task #1: Sector Selection
**Objective:**
| Item | Example |
|---|---|
| **Sector** | Health & Wellness Innovation |
| **Local Challenge** | Barangay health workers still use paper logbooks, causing lost records and missed follow-ups |
| **Target Users** | Barangay health workers and community residents |
| **Proposed Project** | Barangay Health Record App |
| **Key Features** | Offline data entry, vaccination and checkup reminders, high-risk household dashboard |


## Task #2: Zero-Shot Prompting
**Objective:**
Create a simple website to help barangay health workers record and track household health information.

**Exact Prompt:**
> Create a simple website that helps barangay health workers record and track household health information

**Actual Copilot Output:**
  Created a standalone, responsive household health-tracking website in index.html. It includes a dashboard, searchable household register, follow-up statuses, visit logging, and reports. Records are stored in the browser’s local storage.

**What Worked:**
  The review prioritized two concrete usability issues, referenced their implementation locations, and proposed small fixes without expanding scope.

**What Needs Improvement:**
The browser verification was incomplete; the focus-loss and keyboard-scroll behavior still need direct testing.

**Next Action / Verification:**
  Toggle a checklist item using Tab and Space; confirm focus stays on it and completion persists after reload. At a 320–390px viewport, tab to the registry’s scroll region, navigate horizontally to Actions, and confirm its focus indicator and table headings are clear.

## Task #3 Improve: Anatomy of a Prompt
**Objective:**
  Build a responsive, single-page Barangay Health Record website for community health workers, with a household registry, reminders, and a high-risk household dashboard.

**Exact Prompt:**
>   Act as a frontend web developer. Create a responsive single-page Barangay Health Record website for barangay health workers in a local Philippine community. Include a household registry with an add, edit, and remove form, a search and filter bar, a vaccination and checkup reminders section, and a high-risk household dashboard. Use semantic HTML, CSS, and vanilla JavaScript. Do not use external frameworks, backend services, or real personal data, and use fictional sample records only. Provide the required frontend files and implement reminders that show which households are due or overdue for visits. Highlight households with pregnant members, children under 5, or seniors with chronic conditions. The interface must remain readable on mobile screens, and the registry and form must work through mouse and keyboard interaction. Include a notice that the website is a demo and not for real patient data.

**Actual Copilot Output:**
  Updated index.html with the responsive demo website. It includes household add/edit/remove forms, search and filtering, date-based check-up and vaccination reminders, a high-risk household dashboard, and fictional sample records stored in browser storage. A demo-only notice warns users not to enter real patient data.

**What Worked:**
  Static checks confirmed the requested features, mobile layout rules, unique HTML IDs, and JavaScript DOM references. No external frameworks or services are used.

**What Needs Improvement:**
Interactive browser testing was not completed, so keyboard navigation and add/edit/remove/reminder behavior still need a manual check. 

**Next Action / Verification:**
  Open index.html and test adding, editing, and removing a household; searching and filtering; checking due and overdue reminders; and completing the forms using only the keyboard.

## Task 4A — Few-Shot
**Objective:**
Generate four additional household health follow-up items and display them as an interactive checklist.

**Exact Prompt:**
> Create
> household health follow-up checklist items for barangay health workers using
> this format:

> **Example 1:**

> Item: Child vaccination record
> Category: Immunization
> Description: Check that each child under 5 has an up-to-date vaccination
> record.

> **Example 2:**

> Item: Prenatal checkup schedule
> Category: Maternal Care
> Description: Confirm that pregnant members have their next checkup date
> recorded.

> Generate four additional household health follow-up items using the same format and render them as 
> an interactive checklist.

**Actual Copilot Output:**
  Added an interactive checklist to index.html with four items: Chronic medication review, Child growth monitoring, Blood pressure check-in, and Safe water and sanitation. Each includes a category and description. Checkboxes update a completion indicator and save progress in browser storage.

**What Worked:**
  The checklist uses native checkboxes, so it supports mouse and keyboard input. Static checks confirmed all four items, categories, progress display, and persistence wiring.

**What Needs Improvement:**
Interactive browser testing was not completed.

**Next Action / Verification:**
Open index.html, check and uncheck items using the mouse and keyboard, then reload the page to verify saved progress.

## Task 4B — Role Assignment
**Objective:**
  Review the Barangay Health Record website for accessibility issues in semantics, keyboard access, form labels, and visual clarity; recommend targeted improvements without changing scope.

**Exact Prompt:**
>   Act as a frontend accessibility reviewer. Examine the generated Barangay Health Record website (Alaga | Barangay Health Desk). Identify problems involving HTML semantics, keyboard access, form labels, and visual clarity. Recommend targeted improvements without changing the project’s scope.

**Actual Copilot Output:**
  Provided a source-level review of index.html with six recommendations: clarify navigation landmarks, announce single-page view changes, improve text contrast and size, associate validation messages with fields, improve table header and mobile-scroll accessibility, and strengthen focus indicators. Also noted existing accessible features, including labeled form controls, dialog focus management, and native checklist checkboxes.

**What Worked:**
The review identified actionable improvements tied to existing parts of the website and noted accessibility features already in place.

**What Needs Improvement:**
  The review was based on source inspection only; it did not include browser, screen-reader, contrast-measurement, or automated accessibility testing.

**Next Action / Verification:**
  Apply the recommendations in the project, then test keyboard navigation and forms in a browser, verify contrast, and run an accessibility checker.

## Task 5 — Analyze Structured Reasoning and Refinement
**Objective:**
  Review the Barangay Health Record website against its original requirements, identify the two most important implementation issues, and give targeted fixes and verification steps without changing scope.

**Exact Prompt:**
>   Review my Barangay Health Record website (Alaga | Barangay Health Desk) against its original requirements: household registry with add, edit, and remove; search and filter; vaccination and checkup reminders; high-risk household dashboard; follow-up checklist; demo notice; keyboard and mouse use; readable on mobile. Check whether the interactive checklist works correctly, whether the HTML uses appropriate semantic elements, and whether the interface is usable on mobile screens. Identify the two most important implementation issues based on the provided code. Give a concise diagnosis, the smallest appropriate correction for each, and a verification procedure I can follow. Do not change the project’s scope.

**Actual Copilot Output:**
  Reviewed the provided website snapshot and identified two issues: the checklist re-renders after each change and can lose keyboard focus; the horizontally scrollable mobile register is not keyboard-focusable, and the navigation label is on the <aside> instead of the <nav>. Recommended updating checklist elements in place and making the table wrapper keyboard-accessible, naming the navigation landmark, and adding scope="col" to table headers.

**What Worked:**
  The response cited specific code locations, gave small targeted corrections, and included manual verification steps for keyboard and mobile use.

**What Needs Improvement:**
The review was source-based only; it did not confirm behavior in a browser or with a screen reader.

**Next Action / Verification:**
Apply the recommendations in the project’s index.html.

## Task 6 — Compare and Submit
**Objective:**

| Technique | Observation |
|---|---|
| **Zero-Shot** | The AI made a clean household registry with search, filter, Export CSV, and a demo notice. But it left out the vaccination and checkup reminders and the high-risk household dashboard. It only had a basic Follow-ups tab. |
| **Structured Prompt** | Adding role, context, constraints, and acceptance criteria brought in the missing features: reminders with Overdue, Due today, and Upcoming labels, a high-risk households list, and a Risk Flags column. The vaccination list showed only one household, so I still need to check it. |
| **Few-Shot** | The checklist items became consistent. Each one followed the Item / Category / Description format, with a short category and a one-sentence description. The examples controlled the format, but the AI chose new topics like sanitation and postnatal care. |
| **Role Assignment** | The accessibility reviewer role made Copilot check the page instead of adding features. It found low text contrast (about 4.1:1, below the 4.5:1 target), a mobile table that keyboard users can't scroll, repeated "Edit" and "Remove" buttons with the same name, weak table headers, and error messages not linked to fields. |
| **Structured Analysis** | Copilot found that the checklist rebuilds after every toggle, which may make keyboard focus disappear. I tested it with the Tab and Space keys and [focus stayed / focus was lost]. [No fix was needed / I fixed it by updating only the progress text.] |
