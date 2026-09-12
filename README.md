# Tenant Reference Verification & Follow-Up Automation

## Problem
Agents and property managers manually chase previous landlords for 
tenant references. When the landlord doesn't respond, there's no 
consistent follow-up — leads to delayed move-ins and missed red flags.

## How It Works
1. Agent submits applicant details via form
2. System emails previous landlord a 5-question reference form
3. If no response in 48 hours, automatic reminder + agent alert
4. Scheduled backup check catches any case the main flow might miss
5. All data tracked in Google Sheets — no manual entry

## Architecture
- Workflow 1: Applicant Intake (form → Sheet → email)
- Workflow 2: Landlord Response (form → Sheet update)
- Workflow 3: Backup Checker (hourly schedule → catches missed cases)

## Stack
n8n, Google Sheets, Gmail/SMTP, native n8n Forms

## Setup
- Replace placeholder credentials (Google Sheets, SMTP)
- Update form URLs after activating workflows
- Adjust Wait node duration as needed (default: 48 hours)
