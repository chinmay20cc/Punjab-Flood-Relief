# Disaster_Relief_CRM_Salesforce
# Disaster Relief & Donation Management CRM (Punjab Floods)

 Problem Statement

With recent floods in Punjab, NGOs and government relief bodies are facing difficulties in managing donations, tracking relief requests, and assigning volunteers effectively.

* Donors often lose trust when they don’t receive updates about their contributions.
* Volunteers are not properly coordinated.
* Resources don’t always reach the areas in need on time.

*Solution*:A Salesforce-based CRM system called Punjab ReliefConnect CRM that manages donors, volunteers, relief requests, donations, and distribution tracking in real-time.
This ensures transparency, faster volunteer assignment, and accurate reporting to build trust among donors and improve relief operations.



#Phase-by-Phase Implementation

Phase 1: Problem Understanding & Industry Analysis

* Requirement Gathering: Track donations (money, food, medicine, clothes), urgent requests, and donor updates.
* Stakeholders: Admin, Donor Manager, Volunteer Coordinator, Donors, Volunteers, Govt. Officers.
* Business Process: Donor → CRM log → Relief Request → Volunteer Assignment → Distribution → Donor Update → Dashboard.
* Industry Example: NGOs like Red Cross use CRMs for disaster relief.
* AppExchange Exploration: Nonprofit Success Pack (NPSP).

#Phase 2: Org Setup & Configuration

* Salesforce Edition: Developer Org.
* Company Profile: Punjab ReliefConnect CRM.
* Business Hours: 24x7.
* Users: Admin, Donor Manager, Volunteer Coordinator.
* Profiles & Roles: Volunteers (restricted), Donor Manager, Admin.
* OWD & Sharing: Donations private, volunteers see only assigned tasks.
* Sandbox + Deployment: Change Sets to migrate.

#Phase 3: Data Modeling & Relationships

* Custom Objects: Donor, Donation, Volunteer, Relief Request, Distribution.
* Fields: Donation type, Status, Volunteer skills, Request urgency.
* Relationships:

  * Donor → Donation (1\:M).
  * Relief Request ↔ Donation (via Distribution).
  * Volunteer ↔ Distribution (M\:M).
* Record Types: Cash vs Goods donations, Food vs Medical requests.
* Schema Builder: Visualize data model.

#Phase 4: Process Automation (Admin)

* Validation Rule: Donation amount > 0.
* Workflow: Thank-you email after donation.
* Approval Process: High-value donations need Admin approval.
* Flow Builder: Auto-assign nearest volunteer by pincode.
* Custom Notifications: Urgent requests trigger alerts.

#Phase 5: Apex Programming (Developer)

* Trigger: Auto-update Relief Request when fulfilled.
* SOQL: Fetch open urgent requests.
* Batch Apex: Weekly donor impact emails.
* Queueable Apex: Handle bulk donations.
* Scheduled Apex: Daily report of urgent requests.
* Future Methods: Send SMS alerts.
* Test Classes: Validate triggers and jobs.

#Phase 6: User Interface Development

* Lightning App: Punjab ReliefConnect.
* Home Page: Active disasters, donations, requests.
* Record Pages: Donor history, Volunteer tasks.
* Tabs: Donors, Donations, Volunteers, Requests, Distributions.
* LWC Components:

  * Nearby Requests Finder.
  * Donor Impact Dashboard.

#Phase 7: Integration & External Access

* Google Maps API: Locate relief centers.
* Govt. Disaster API: Import flood alerts.
* Platform Events: Urgent request notifications.
* Experience Cloud: Donor portal.
* OAuth: Secure donor logins.

#Phase 8: Data Management & Deployment

* Data Import Wizard: Donor/volunteer records.
* Data Loader: Bulk uploads.
* Duplicate Rules: Prevent duplicates.
* Data Export: Weekly backups.
* Deployment: Change Sets, VS Code + SFDX.

#Phase 9: Reporting, Dashboards & Security Review

* Reports: Donations by type, Volunteers by district, Requests fulfilled vs pending.
* Dashboards: Punjab Relief Impact Tracker.
* Dynamic Dashboards: Volunteers see only assigned tasks.
* Security: Donors see only their own donations.
* Audit Trail: Track changes.


#Phase 10: Final Presentation & Demo Day

* Pitch: Punjab ReliefConnect ensures transparency and efficiency in disaster relief.
* Demo Flow: Donor logs donation → Request auto-matched → Volunteer assigned → Delivery → Dashboard update.
* Handoff Docs: Setup + user manuals.
* Portfolio: Showcase project on LinkedIn/GitHub.

