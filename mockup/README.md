# ARM v4 portal mockups

Both mockups use illustrative data and are not the real portal. Open the `.html` file in a browser; the tabs and the request detail panel are clickable.

## Scenario A: ARM creates worklists (`v4/`)

Based on the concept deck (slide 6: "Automate worklists generation from ARM").

- ARM owns the request lifecycle and the worklist builder.
- Users select requests in the Requests grid and create a worklist in ARM, which sends it to the instrument through LEAP.
- Request detail has cancel, add method and reopen actions.

## Scenario B: LEAP drives the flow, ARM shows status (`v4-scenario-b-leap-driven/`)

Based on the TO-BE flow diagram (ChemDiary -> LEAP -> instruments -> LDI -> LEAP -> ChemDiary, with status to ARM).

- ChemDiary sends the request to Lab Automation (LEAP). LEAP creates and sends worklists to the instruments (formats 10p, txt, spl).
- Instruments write result files (XLS/TXT, PS, RPT) into the Lab Data Inventory; LEAP reads them and registers results in ChemDiary.
- LEAP sends status to ARM. ARM is a read-only view: Requests grid, Worklists tab, dashboard, flow/data model/glossary and release notes.
- `ARM_TOBE_Flow.png` / `.svg` is a clean redraw of the flow as read from the diagram.

## Open points for Scenario B

- Meaning of the worklist formats 10p, txt and spl (labels taken from the diagram).
- What the pink assistant icon next to the LDI catalog represents.
- Whether ARM issues its own request ID or mirrors LEAP and ChemDiary IDs.

The choice between A and B decides who owns worklist generation (ARM or LEAP) and whether ARM has any write actions.
