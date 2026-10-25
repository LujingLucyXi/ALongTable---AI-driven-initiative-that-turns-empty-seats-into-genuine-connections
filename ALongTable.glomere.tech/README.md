# ALongTable.glomere.tech prototype

Bilingual restaurant-table booking prototype with interest onboarding, recommended tables, prepaid menu customization, and host-created gatherings.

## Included flows

- Choose multiple themes to personalize tables-to-join recommendations.
- Browse seeded, already-populated tables across all themes, with occupied chairs, open seats, and live seat counts.
- Join a recommended table through the prepaid menu, course selection, dish pickers, seat selection, and checkout.
- Create a restaurant table at least 48 hours before its start time. A host completes the prepaid menu and seat flow before the table is published.
- At 24 hours before the gathering, the prototype marks a table as cancelled if it is below its minimum guest count; otherwise it locks the table.

Table data is held in the widget bridge when available, with in-memory state otherwise. The timer checks every minute while the widget is open and recalculates when persistent bridge state loads. A production deployment would need a server-side scheduled job for reliable cancellation while the client is closed.
