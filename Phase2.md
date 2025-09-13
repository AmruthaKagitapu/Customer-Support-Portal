# Phase 2 — Org Setup & Configuration

**Project:** Customer Support Portal (Salesforce Service Cloud)
**Context:** As a 4th-year student, my objective is to set up a Salesforce org just as a consultant/administrator would for a telecom customer support solution. Completing this baseline configuration will support later case automation, portal flows, and management dashboards.


## 1. Salesforce Editions

* Using a Developer Edition org for full feature access at no cost.
* Note: Real companies often use Enterprise or Unlimited to support more users, advanced security, and integration.

## 2. Company Profile Setup

* Set company name, address, primary time zone (e.g., Asia/Kolkata), and currency (INR/USD).
* These settings ensure cases, emails, and escalation timings match the company's operations.

## 3. Business Hours & Holidays

* Configured standard business hours (Mon–Fri, 9 AM–6 PM) to reflect support team uptime.
* Added national and company holidays (e.g., Diwali, Independence Day) so SLAs and escalations reflect actual working days.

## 4. Fiscal Year Settings

* Used standard fiscal year (Jan–Dec) for company reporting.
* Real-world note: Custom fiscal years are configured for telecom or regional reporting needs when required.

## 5. User Setup & Licenses

* Created sample users: Support Agent, Manager, IT Administrator, Customer Portal User.
* Assigned standard Salesforce licenses (Service Cloud for support users, Community licenses for portal users).

## 6. Profiles

* Support Agent Profile: full access to case objects and reporting.
* Manager Profile: broader access including agent records, dashboards, and escalations.
* Portal User Profile: limited access—can create/view own cases.

## 7. Roles

* Hierarchical roles reflecting telecom support:
Support Manager → Support Agent → Customer Portal User
* Record visibility flows upward; managers see team activity, agents see their own, portal users see only their interactions.

## 8. Permission Sets

* “Escalation Supervisor” for managers who need extra permissions to reassign cases.
* “Knowledge Contributor” for agents who draft and publish FAQ/knowledge articles.

## 9. Organization-Wide Defaults (OWD)

* Cases: Private (agents/managers see only their team’s cases).
* Knowledge Articles: Public Read Only (customers can view).

## 10. Sharing Rules

* Example: Automatically share high-priority cases with managers for immediate response.
* Rule: Cases escalated to “Urgent” are shared with entire support team.

## 11. Login Access Policies

* Set trusted IP ranges for support agents (workplace security).
* Enabled two-factor authentication for admins and managers to secure sensitive data.

## 12. Dev Org Setup

* Connected Developer Org to VS Code and GitHub for tracking configuration changes.
* Practiced using Salesforce DX scratch orgs to test features as an admin would.

## 13. Sandbox Usage

* Developer Edition provides a single sandbox for testing new workflows.
* Simulated: Build automation in sandbox, then deploy to main org for “production”-like workflow.

## 14. Deployment Basics

* Leveraged change sets for simple deployments of objects and workflows.
* Explored Git-based deployments to track changes and enable teamwork, following real-world DevOps best practices.