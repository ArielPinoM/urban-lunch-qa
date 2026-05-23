# Mobile QA Portfolio: Urban.Lunch Android Application Testing

## Project Overview
This repository contains the comprehensive QA testing documentation and verification artifacts for the initial Android release of **Urban.Lunch**, a mobile application designed for food delivery at designated pick-up points. 

The primary objective of this project was to validate the core functional requirements, ensure application stability, and verify end-to-end user workflows during the Software Test Life Cycle (STLC). Testing was executed from a black-box perspective, focusing on functional verification, UI/UX consistency, and error handling.

---

## Tech Stack & Tools
*   **Platform:** Android OS
*   **IDE & Log Analysis:** Android Studio
*   **Defect Tracking & Management:** Jira
*   **Test Design & Documentation:** Google Sheets / Markdown

---

## Testing Scope
The scope of validation focuses entirely on the core functional requirements and workflow mechanics of the application, broken down into five distinct modules:

### 1. Pick-up Point Selection
> 📌 [Requirements Matrix](./docs/requirements/01_pickup_points_specs.md)

*   **Map Visualization:** Verification that all available collection nodes render properly on the interactive map.
*   **Default State:** Ensuring no pick-up point is selected by default upon screen initialization.
*   **Selection States:** Validating that tapping a point switches its visual indicator to black (Active/Selected) and that a repeated tap toggles it back to unselected.
*   **Focus Management:** Verifying that selecting a new pick-up point shifts focus immediately and deselects the previously active one.

### 2. Dish Selection
> 📌 [Requirements Matrix [PENDING]](./docs/requirements/)

*   **Dish List UI & Navigation:** 
    *   Verifying item container components (Name, '+/-' modifiers, item counter, and details arrow).
    *   Validating that tapping any area of the item row (excluding '+/-' buttons) navigates the user to the Dish Details screen.
*   **Cart Operations:** 
    *   Tapping '+' increments the counter and assigns the order allocation to the closest restaurant relative to the chosen pick-up point.
    *   Tapping '-' decrements the counter and removes the item instance from the current order list.
*   **Footer Progress Bar:** Verifying dynamic status transitions where Step 1 is highlighted as 'Completed' and Step 2 is set to 'In Progress'.
*   **Dish Details Specification:** 
    *   Validating content layout hierarchy (Photo, description, ingredients list, and restaurant origin).
    *   Testing back-navigation using the explicit arrow anchor.
    *   Ensuring the 'Next' checkout button remains disabled until at least one item is present in the order list.

### 3. Order Confirmation
> 📌 [Requirements Matrix [PENDING]](./docs/requirements/)

*   **Screen Layout Verification:** Validating the layout matrix containing the Pick-up Point name, 'Back' navigation button, item summary list, total aggregate cost, estimated delivery ETA, and the operational footer.
*   **UI Constraints:** Verifying scrollability and list view scrolling performance for long, multi-item orders.
*   **Total Cost Algorithm:** Validating that the final total dynamically balances the mathematical sum of all dishes, preparations, and specific delivery fees.
*   **Footer Status Integration:** Step 1 & 2 marked as 'Completed', with Step 3 active as 'In Progress'.
*   **Workflow Transition:** Tapping the 'Order' button successfully processes the state change and routes the user to the Order Tracking view.

### 4. Real-Time Order Tracking
> 📌 [Requirements Matrix [PENDING]](./docs/requirements/)

*   **Map & Routing Logic:** Verifying concurrent rendering of the target pick-up point, preparing restaurant nodes, active courier routes, unit line pricing per restaurant, preparation countdown timers, and individual delivery transit ETAs.
*   **Dynamic Lists:** Scroll verification for heavy data sets inside the status cards.
*   **Timer Lifecycle:** Tracking the global countdown timer behavior. Upon full completion/delivery of all items, the timer must hit zero and automatically trigger the screen transition to 'Order Dispatched'.

### 5. Order Dispatched & Error Notifications
> 📌 [Requirements Matrix [PENDING]](./docs/requirements/)

*   **Order Completion Flow:** Automated state transition upon countdown timeout, displaying the pick-up point vector anchor, routing the user to the Feedback screen upon action click, and resetting the app state back to Pick-up Selection for clean sequence replication.
*   **Error Handling & Exception Handling:**
    *   **System Permissions:** Graceful error notification deployment when device location access permissions are explicitly denied.
    *   **Business Logic Boundaries:** Triggering an explicit validation error notification when an order submission is attempted with an empty cart state.

---

## Test Environment
*   **Testing Approach:** 100% Physical Device Testing (No emulators utilized)
*   **Physical Test Device:** Samsung Galaxy S23+ (Model: SM-S916U)
*   **Operating System:** Android 16 (One UI 8.0)
*   **Application Build Version:** v1.0

---

## Test Execution Results

The testing life cycle is executed iteratively per module. Below is the current cumulative execution status:

| Module ID | Test Suite / Functional Component | Total TCs | 🟢 Passed | 🔴 Failed | 🟡 Skipped | ⚪ Pending | Progress (%) |
| :---: | :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **01** | Pick-up Point Selection | 6 | 6 | 0 | 0 | 0 | 100% |
| **02** | Dish Selection (List & Details) | 0 | 0 | 0 | 0 | 0 | 0% |
| **03** | Order Confirmation & Checkout | 0 | 0 | 0 | 0 | 0 | 0% |
| **04** | Real-Time Order Tracking | 0 | 0 | 0 | 0 | 0 | 0% |
| **05** | Order Dispatched & Error Notifications | 0 | 0 | 0 | 0 | 0 | 0% |
| **Total** | **Cumulative Metrics** | **6** | **6** | **0** | **0** | **0** | **xx%** |

---

## Defect Metrics (Jira)
<!-- [Pending user data input] -->
*This section will contain defect analysis, including distribution by priority (Critical, High, Medium, Low) and breakdown per module.*

---

## Test Summary Report & Conclusions
<!-- [Pending user data input] -->
*This section will deliver the final assessment of the application's quality state, deployment readiness, and outstanding risks.*