Task 2 — Zero - Shot Prompt
Objective:
Create a simple website to help barangay health workers record and track household health information.

Exact Prompt:
Create a simple website that helps barangay health workers record and track household health informatio

Actual Copilot Output:
Created a standalone, responsive household health-tracking website in index.html. It includes a dashboard, searchable household register, follow-up statuses, visit logging, and reports. Records are stored in the browser’s local storage.

The site includes sample records and working forms for adding households and recording visits. Household search and status filters update the register, and the layout adapts to smaller screens.

What Needs Improvement:
Browser interaction testing was not completed. The local-storage approach is suitable for a prototype, not for storing real or sensitive health information.

Next Action / Verification:
Open index.html in a browser. Test adding a household, filtering the register, logging a visit, and reloading to check that records persist.

Task 3 — Structured Prompting (Anatomy of a Prompt)
Objective: 
Build a responsive, single-page Barangay Health Record website for community health workers, with a household registry, reminders, and a high-risk household dashboard.

Exact Prompt: 
Act as a frontend web developer. Create a responsive single-page Barangay Health Record website for barangay health workers in a local Philippine community. Include a household registry with an add, edit, and remove form, a search and filter bar, a vaccination and checkup reminders section, and a high-risk household dashboard. Use semantic HTML, CSS, and vanilla JavaScript. Do not use external frameworks, backend services, or real personal data, and use fictional sample records only. Provide the required frontend files and implement reminders that show which households are due or overdue for visits. Highlight households with pregnant members, children under 5, or seniors with chronic conditions. The interface must remain readable on mobile screens, and the registry and form must work through mouse and keyboard interaction. Include a notice that the website is a demo and not for real patient data.

Actual Copilot Output:
Updated index.html with the responsive demo website. It includes household add/edit/remove forms, search and filtering, date-based check-up and vaccination reminders, a high-risk household dashboard, and fictional sample records stored in browser storage. A demo-only notice warns users not to enter real patient data.

What Worked:
Static checks confirmed the requested features, mobile layout rules, unique HTML IDs, and JavaScript DOM references. No external frameworks or services are used.

What Needs Improvement:
Interactive browser testing was not completed, so keyboard navigation and add/edit/remove/reminder behavior still need a manual check. Browser storage is for demo use only and is not appropriate for real health records.

Next Action / Verification:
Open index.html and test adding, editing, and removing a household; searching and filtering; checking due and overdue reminders; and completing the forms using only the keyboard.

Task 4A: Few-Shot Prompting
Objective: Generate four additional household health follow-up items and display them as an interactive checklist.

Exact Prompt:
Create household health follow-up checklist items for barangay health workers using this format:

Example 1:
Item: Child vaccination record
Category: Immunization
Description: Check that each child under 5 has an up-to-date vaccination record.

Example 2:
Item: Prenatal checkup schedule
Category: Maternal Care
Description: Confirm that pregnant members have their next checkup date recorded.

Generate four additional household health follow-up items using the same format and render them as an interactive checklist

**Actual Copilot Output:**

Added an interactive checklist to index.html with four items: Chronic medication review, Child growth monitoring, Blood pressure check-in, and Safe water and sanitation. Each includes a category and description. Checkboxes update a completion indicator and save progress in browser storage.

What Worked:
The checklist uses native checkboxes, so it supports mouse and keyboard input. Static checks confirmed all four items, categories, progress display, and persistence wiring.

What Needs Improvement:
Interactive browser testing was not completed.

Next Action / Verification:
Open index.html, check and uncheck items using the mouse and keyboard, then reload the page to verify saved progress.

Task 4B: Role Assignment (Accessibility Review)

Objective:
Exact Prompt:
Act as a frontend accessibility reviewer. Examine the generated Barangay Health Record website (Alaga | Barangay Health Desk). Identify problems involving HTML semantics, keyboard access, form labels, and visual clarity. Recommend targeted improvements without changing the project’s scope.

Actual Copilot Output:
Provided a source-level review of index.html with six recommendations: clarify navigation landmarks, announce single-page view changes, improve text contrast and size, associate validation messages with fields, improve table header and mobile-scroll accessibility, and strengthen focus indicators. Also noted existing accessible features, including labeled form controls, dialog focus management, and native checklist checkboxes.

What Worked:
The review identified actionable improvements tied to existing parts of the website and noted accessibility features already in place.

What Needs Improvement:
The review was based on source inspection only; it did not include browser, screen-reader, contrast-measurement, or automated accessibility testing

Next Action / Verification:
Apply the recommendations in the project, then test keyboard navigation and forms in a browser, verify contrast, and run an accessibility checker.

Task 5: Structured Analysis and Refinement

Objective:

Exact Prompt:
Review my Barangay Health Record website (Alaga | Barangay Health Desk) against its original requirements: household registry with add, edit, and remove; search and filter; vaccination and checkup reminders; high-risk household dashboard; follow-up checklist; demo notice; keyboard and mouse use; readable on mobile. Check whether the interactive checklist works correctly, whether the HTML uses appropriate semantic elements, and whether the interface is usable on mobile screens. Identify the two most important implementation issues based on the provided code. Give a concise diagnosis, the smallest appropriate correction for each, and a verification procedure I can follow. Do not change the project’s scope.

Actual Copilot Output:
Reviewed the provided website snapshot and identified two issues: the checklist re-renders after each change and can lose keyboard focus; the horizontally scrollable mobile register is not keyboard-focusable, and the navigation label is on the <aside> instead of the <nav>. Recommended updating checklist elements in place and making the table wrapper keyboard-accessible, naming the navigation landmark, and adding scope="col" to table headers.

What Worked:
The response cited specific code locations, gave small targeted corrections, and included manual verification steps for keyboard and mobile use.

What Needs Improvement:
The review was source-based only; it did not confirm behavior in a browser or with a screen reader.

Next Action / Verification:
Apply the recommendations in the project’s index.html. Then test checkbox focus and persistence with Tab and Space, and test register scrolling with touch and keyboard at a 320–375px viewport.

Task 6: Compare and Submit

