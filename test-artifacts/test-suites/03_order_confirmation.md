# Test Suite: Order Confirmation & Checkout
**Module Focus:** Verification of summary layout components, aggregate cost calculation, scrolling constraints, and checkout routing.
> 📌 [Order Confirmation Requirements](../../docs/requirements/03_order_confirmation_specs.md#functional-requirements-specification-order-confirmation)

| Test ID | Component / Feature | Test Condition (Verification Step) | Expected Result | Status |
| :--- | :--- | :--- | :--- | :---: |
| **TC-OC-001** | Pick-up Point Label | Select Enigma as the pickup point and navigate to the Checkout screen. | The screen explicitly displays the correct name (Enigma) of the chosen Pick-up Point. | 🟢 PASSED |
| **TC-OC-002** | Back Button Navigation | Tap the "Back" button on the Order Confirmation view. | The application safely terminates the checkout view and returns to the previous screen. | 🟢 PASSED |
| **TC-OC-003** | Estimated Delivery ETA | Verify the delivery text block on screen initialization. | The interface displays the estimated delivery ETA for collection at the pick-up node. | 🟡 SKIPPED<br>[Gray Area] The requirements specify that the estimated delivery time should be displayed. However, the attached Order Confirmation screen design does not display the estimated delivery time. |
| **TC-OC-004** | UI Scrollability | Populate the cart with an extensive list of items that exceeds screen height. | The item list responds to vertical drag gestures, allowing smooth scrolling. | 🟢 PASSED |
| **TC-OC-005** | Calculation: Dishes | Verify the total breakdown calculation with multiple items. | The total accurately reflects the mathematical sum of all base dish prices. | 🟢 PASSED |
| **TC-OC-006** | Progress Bar Step 1 & 2| View the footer progress bar layout on screen load. | Step 1 and Step 2 are explicitly marked as completed '✓' via their green colored assets. | 🟢 PASSED |
| **TC-OC-007** | Progress Bar Step 3 | View the footer progress bar layout on screen load. | Step 3 (Order Confirmation) is highlighted active as in progress '3'. | 🟢 PASSED |
| **TC-OC-008** | Order Submission Flow | Tap the "Order" ("Pedir") button with a valid cart configuration. | The checkout transaction triggers and transitions the user to the Order Tracking view. | 🟢 PASSED |