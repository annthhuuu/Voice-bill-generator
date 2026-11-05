# Software Requirements Specification

## 1. Purpose and Scope
The AI Voice Bill Generator is a proposed system that accepts spoken billing details, converts them into structured items, calculates totals, and presents a bill for user confirmation.

## 2. Users
- Shopkeeper or cashier
- Administrator (only if product/user management is included)

## 3. Functional Requirements
- FR-01: Capture voice input from the user.
- FR-02: Convert captured speech into text.
- FR-03: Extract product names and quantities.
- FR-04: Validate products against the product catalogue.
- FR-05: Retrieve or enter unit prices.
- FR-06: Calculate line totals and bill total.
- FR-07: Display a bill preview before finalization.
- FR-08: Allow correction or removal of incorrectly recognized items.
- FR-09: Save or export a confirmed bill.
- FR-10: Display useful errors for unclear speech or unknown products.

## 4. Non-Functional Requirements
- Usability: simple workflow and clear feedback.
- Accuracy: calculations must be correct and repeatable.
- Reliability: unclear input must not silently create a finalized bill.
- Security: protect stored bills and product information.
- Maintainability: separate modules and testable components.
- Accessibility: provide manual correction as an alternative to voice.

## 5. Assumptions and Constraints
A microphone/audio source is available. Speech recognition may depend on network connectivity and the selected provider. Supported languages, currency, tax rules, technology stack, and database are still to be decided.

## 6. Acceptance Criteria
A user can enter supported voice details, review extracted items, correct errors, see a correct calculated total, and save/export only after confirmation.
