# Test Suite: Order Dispatched & Error Notifications
**Module Focus:** Verification of automatic lifecycle transitions, destination map rendering, sequential feedback routing, and business rule error blocks.
> 📌 [Order Dispatched & Errors Requirements](../../docs/requirements/05_order_dispatched_specs.md#functional-requirements-specification-order-dispatched--error-notifications)

| Test ID | Component / Feature | Test Condition (Verification Step) | Expected Result | Status | Bug Report Link |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **TC-OD-001** | Map Node Render | Inspect the map layout on the "Order Dispatched" screen. | The map explicitly renders the visual pin of the chosen Pick-up Point destination. | 🟢 PASSED |
| **TC-OD-002** | Completion: Feedback | Tap the primary completion action button on the success screen. | The application successfully routes the user to the Feedback page. | 🟢 PASSED |
| **TC-OD-003** | Completion: Reset | Complete the feedback interaction on the Feedback page. | The application redirects the user back to the Module 01 Pick-up Point selection screen to start a new order. | 🟢 PASSED |
| **TC-OD-004** | Permission Intercept | Launch the application or trigger map features while system location permissions are set to "Deny". | An explicit error notification message regarding missing geolocation access appears on the screen. | 🟢 PASSED |
| **TC-OD-005** | Empty Order Intercept| Navigate to the checkout phase and attempt to press the checkout trigger with zero items in the cart. | An explicit error notification message stating that an order cannot be created empty is displayed. | 🟢 PASSED |