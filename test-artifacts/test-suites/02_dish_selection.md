# Test Suite: Dish Selection (List & Details)
**Module Focus:** Verification of item list mechanics, cart allocation logic, layout integrity, and screen state transitions.
> 📌 [Dish Selection Requirements](../../docs/requirements/02_dish_selection_specs.md#functional-requirements-specification-dish-selection)

| Test ID | Component / Feature | Test Condition (Verification Step) | Expected Result | Status | Bug Report Link |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **TC-DS-001** | List UI Layout | Initialize the Dish List view and check items elements. | Each item row displays the name, '+' button, '-' button, counter, and details arrow. | 🟢 PASSED |
| **TC-DS-002** | Navigation Vector | Tap on the row body/text area of a specific dish item. | The application intercepts the event and navigates to the Dish Details screen. | 🟢 PASSED |
| **TC-DS-003** | Cart Counter (List) | Tap the '+' button on a dish item from the list view. | The item counter increments exactly by 1 unit. | 🟢 PASSED |
| **TC-DS-004** | Order Allocation | Tap the '+' button on a dish item from the dish details view. | The dish is added to the order from the closest restaurant relative to the pick-up point. | 🟢 PASSED |
| **TC-DS-005** | Cart Counter (List) | Tap the '-' button on an item with an active count of 1. | The item counter decrements to 0 and the item is removed from the active order list. | 🟢 PASSED |
| **TC-DS-006** | Progress Bar Step 1 | View the footer progress bar on the Dish List screen. | Step 1 (Pick-up Point) is explicitly marked as completed '✓' with its green colored indicator. | 🟢 PASSED |
| **TC-DS-007** | Progress Bar Step 2 | View the footer progress bar on the Dish List screen. | Step 2 (Dish Selection) is explicitly marked as in progress '2'. | 🟢 PASSED |
| **TC-DS-008** | Detail Layout UI | Open the Details view for any selected dish item. | The screen displays the photo, general description, ingredients list, and restaurant label. | 🟢 PASSED |
| **TC-DS-009** | Detail Back Anchor | Tap the back arrow icon situated to the left of the dish name. | The details view closes and returns the user to the main Dish List screen. | 🟢 PASSED |
| **TC-DS-010** | Cart Counter (Detail)| Tap the '+' button from within the Dish Details screen. | The dish is successfully added and increments the global order list structure. | 🟢 PASSED |
| **TC-DS-011** | Checkout Guardrail | Initialize the view with an empty cart state (0 items). | The 'Next' checkout routing button is visually greyed out and completely inactive. | 🟢 PASSED |