# Test Suite: Real-Time Order Tracking
**Module Focus:** Verification of multi-node map rendering, dynamic cost/ETA overlays, list scrollability, and automated timer screen transitions.
> 📌 [Order Tracking Requirements](../../docs/requirements/04_order_tracking_specs.md#functional-requirements-specification-real-time-order-tracking)

| Test ID | Component / Feature | Test Condition (Verification Step) | Expected Result | Status | Bug Report Link |
| :--- | :--- | :--- | :--- | :--- | :---: |
| **TC-OT-001** | Map Node: Pick-up Point| Initialize the Tracking screen and inspect map anchors. | The targeted pick-up point vector icon renders correctly on the map layer. | 🟢 PASSED |
| **TC-OT-002** | Map Node: Restaurants | Initialize the Tracking screen and inspect map anchors. | All restaurant nodes involved in preparing the active order render as distinct icons. | 🟢 PASSED |
| **TC-OT-003** | Map Layers: Delivery Routes | Initialize the Tracking screen and inspect map lines. | The active courier route paths from each restaurant to the pick-up point are drawn clearly. | 🟢 PASSED |
| **TC-OT-004** | Overlay Data: Cost | Inspect the overlay metric box for an active restaurant pin. | The label accurately displays the sum cost of the specific dishes assigned to that location. | 🔴 FAILED | [BUG-001](../../bug-reports/bug-001.md#bug-001) |
| **TC-OT-005** | Overlay Data: Preparation | Inspect the overlay metric box for an active restaurant pin. | The card shows the dynamic remaining preparation countdown for that shop. | 🔴 FAILED | [BUG-002](../../bug-reports/bug-002.md#bug-002) |
| **TC-OT-006** | Overlay Data: Transit ETA | Inspect the overlay metric box for an active restaurant pin. | The card displays the real-time delivery transit ETA to the pick-up point. | 🔴 FAILED | [BUG-003](../../bug-reports/bug-003.md#bug-003) |
| **TC-OT-007** | Tracking List Scroll | Generate a large order that populates a dense tracking list. | The layout responds to swipe gestures, permitting vertical scrolling without cutting content. | 🟢 PASSED |
| **TC-OT-008** | Global Tracker Clock | View the main tracking header component upon initialization. | A master countdown timer accurately displays the total aggregate time remaining for fulfillment. | 🟢 PASSED |
| **TC-OT-009** | Lifecycle Auto-Transition | Monitor the view until the master countdown clock strikes zero (0:00). | The screen automatically terminates and routes the user to the "Order Dispatched" view. | 🟢 PASSED |