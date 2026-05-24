# Test Suite: Pick-up Point Selection
**Module Focus:** Verification of map rendering states, selection toggles, and state transitions for delivery points.
> 📌 [Pickup Point Selection Requirements](../../docs/requirements/01_pickup_points_specs.md#functional-requirements-specification-pick-up-point-selection)

| Test ID | Component / Feature | Test Condition (Verification Step) | Expected Result | Status | Bug Report Link |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **TC-PP-001** | Initial Map State | Launch the application and load the Pick-up Point selection screen. | The interactive map renders all available pick-up points. No point is selected by default. | 🟢 PASSED |
| **TC-PP-002** | Selection State | Tap an unselected pick-up point icon on the map. | The selected point changes its visual state to black color and is marked active. | 🟢 PASSED |
| **TC-PP-003** | Deselection Toggle | Tap a currently selected (black) pick-up point icon for a second time. | The selection is cancelled; the icon returns to its default unselected state. | 🟢 PASSED |
| **TC-PP-004** | Selection Switch | Tap a new pick-up point while a different point is already selected. | Focus shifts immediately; previous point deselects and the new point changes to black. | 🟢 PASSED |
| **TC-PP-005** | UI Responsiveness | Rapidly alternate taps between multiple close-proximity pick-up points. | Map selection state updates without UI lagging, ghost selections, or app freezing. | 🟢 PASSED |
| **TC-PP-006** | State Persistence | Background the app with an active selection, wait 1 minute, and resume. | The selected pick-up point remains active and highlighted in black upon resume. | 🟢 PASSED |